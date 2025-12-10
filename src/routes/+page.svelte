<script>
  import Navbar from '$lib/components/Navbar.svelte';
  import Hero from '$lib/components/Hero.svelte';
  import Logos from '$lib/components/Logos.svelte';
  import WhyDiligenced from '$lib/components/WhyEcho.svelte';
  import Products from '$lib/components/Products.svelte';
  import Founders from '$lib/components/Founders.svelte';
  import FAQ from '$lib/components/FAQ.svelte';
  import BottomCTA from '$lib/components/BottomCTA.svelte';
  import Footer from '$lib/components/Footer.svelte';
</script>

<svelte:head>
  <title>Diligenced | Investor-Grade Market Research in Days</title>
  <meta name="description" content="AI-moderated expert interviews and automated synthesis deliver the insights PE deal teams need for pre-LOI diligence—faster than traditional consulting." />
  <meta property="og:title" content="Diligenced | Investor-Grade Market Research in Days" />
  <meta property="og:description" content="AI-moderated expert interviews and automated synthesis deliver the insights PE deal teams need for pre-LOI diligence—faster than traditional consulting." />
  <meta property="og:type" content="website" />
  <meta name="twitter:card" content="summary_large_image" />
  <meta name="twitter:title" content="Diligenced | Investor-Grade Market Research in Days" />
  <meta name="twitter:description" content="AI-moderated expert interviews and automated synthesis deliver the insights PE deal teams need for pre-LOI diligence—faster than traditional consulting." />
</svelte:head>

<div class="min-h-screen bg-[#f5f5f5] font-sans selection:bg-black selection:text-white">
  <Navbar />
  <Hero />
  <Logos />
  <WhyDiligenced />
  <Products />
  <Founders />
  <FAQ />
  <BottomCTA />
  <Footer />
</div>

