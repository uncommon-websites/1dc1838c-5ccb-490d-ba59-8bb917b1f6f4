<script lang="ts">
  import { slide } from 'svelte/transition';
  
  interface FAQItem {
    question: string;
    answer: string;
  }

  const faqs: FAQItem[] = [
    { question: "How does Diligenced compare to traditional consulting firms?", answer: "Diligenced delivers the same investor-grade quality as firms like Bain and BCG, but in days instead of weeks. Our AI-moderated interviews and automated synthesis reduce turnaround time by 70% while maintaining the depth and rigor PE deal teams require for pre-LOI diligence." },
    { question: "What types of research does Diligenced provide?", answer: "We specialize in pre-LOI commercial due diligence for private equity deal teams. This includes market sizing, competitive landscape analysis, customer interviews, and industry expert insights—everything you need to make confident investment decisions before signing a letter of intent." },
    { question: "How quickly can I get results?", answer: "Most projects are delivered in 3-5 days. We understand that PE deal timelines are tight, especially in competitive processes. Our AI-powered platform enables us to conduct and synthesize expert interviews faster than traditional methods without sacrificing quality." },
    { question: "Who conducts the interviews?", answer: "Our proprietary AI conducts interviews with industry experts, customers, and competitors. The AI is trained to ask probing follow-up questions and gather the nuanced insights you'd expect from experienced consultants. All interviews are then reviewed and synthesized by our team of former Blackstone, BCG, and Bain professionals." },
    { question: "How much does Diligenced cost compared to traditional consulting?", answer: "Our pricing is significantly lower than traditional consulting firms while delivering comparable quality. Contact us for a custom quote based on your specific research needs and deal parameters." },
    { question: "What industries do you cover?", answer: "We cover all major industries relevant to private equity investing. Our AI interview platform is industry-agnostic, and our team has experience across technology, healthcare, financial services, consumer goods, and industrial sectors." },
    { question: "Can I see a sample report?", answer: "Yes! We're happy to share sample reports with qualified PE professionals. Request a demo to see examples of our work and discuss how we can support your deal pipeline." }
  ];

  let openIndex: number | null = null;

  function toggle(index: number) {
    openIndex = openIndex === index ? null : index;
  }
</script>

<section class="bg-[#f5f5f5] px-6 py-24">
  <div class="max-w-[1400px] mx-auto grid grid-cols-1 lg:grid-cols-12 gap-12">
    <div class="lg:col-span-4">
      <h2 class="font-serif text-4xl text-gray-900 mb-6">
        Frequently asked questions
      </h2>
      <a href="/" class="text-sm text-gray-900 border-b border-gray-300 pb-0.5 hover:border-black transition-colors">See all support</a>
    </div>
    
    <div class="lg:col-span-8">
      <div class="border-t border-gray-200">
        {#each faqs as faq, i}
          <div class="border-b border-gray-200">
            <button 
              class="w-full py-6 flex justify-between items-center text-left hover:bg-gray-50 transition-colors"
              on:click={() => toggle(i)}
            >
              <span class="text-lg text-gray-800">{faq.question}</span>
              <span class="text-2xl font-light text-gray-400 ml-4">
                {openIndex === i ? '−' : '+'}
              </span>
            </button>
            {#if openIndex === i}
              <div transition:slide class="pb-6 text-gray-500 leading-relaxed">
                {faq.answer}
              </div>
            {/if}
          </div>
        {/each}
      </div>
    </div>
  </div>
</section>
