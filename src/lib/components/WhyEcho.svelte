<script>
  import SectionLabel from './SectionLabel.svelte';
</script>

<section class="bg-[#f5f5f5] px-6 py-24">
  <div class="max-w-[1400px] mx-auto grid grid-cols-1 lg:grid-cols-12 gap-12">
    <div class="lg:col-span-3">
      <SectionLabel label="Why Diligenced" />
    </div>
    
    <div class="lg:col-span-9 grid grid-cols-1 md:grid-cols-2 gap-16">
      <div>
        <h2 class="font-serif text-3xl md:text-4xl leading-tight text-gray-900 mb-6">
          Replace weeks of traditional consulting with days of AI-powered research
        </h2>
        <p class="text-gray-500 leading-relaxed">
          Built by former Blackstone, BCG, and Bain professionals who understand the speed and quality PE deal teams need for pre-LOI diligence.
        </p>
      </div>
      
      <div class="flex gap-12 items-end pb-2">
        <div class="flex flex-col gap-1">
            <span class="text-4xl font-serif text-gray-900 mb-1">3-5 days</span>
            <span class="text-xs text-gray-400">average delivery time</span>
        </div>
        <div class="flex flex-col gap-1">
            <span class="text-4xl font-serif text-gray-900 mb-1">$8B</span>
            <span class="text-xs text-gray-400">CDD market opportunity</span>
        </div>
      </div>
    </div>
  </div>
</section>
