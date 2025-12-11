<script lang="ts">
  import Header from "$lib/components/Header.svelte";
  
  // Icons
  const ArrowRight = `<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>`;
  const PlayCircle = `<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><polygon points="10 8 16 12 10 16 10 8"/></svg>`;
  const ChevronLeft = `<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m15 18-6-6 6-6"/></svg>`;
  const ChevronRight = `<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m9 18 6-6-6-6"/></svg>`;
  const Check = `<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"><path d="M20 6 9 17l-5-5"/></svg>`;
  const Plus = `<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="M12 5v14"/></svg>`;
  const Instagram = `<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect width="20" height="20" x="2" y="2" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" x2="17.51" y1="6.5" y2="6.5"/></svg>`;
  const LinkedIn = `<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect width="4" height="12" x="2" y="9"/><circle cx="4" cy="4" r="2"/></svg>`;
  const XIcon = `<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M18 6 6 18"/><path d="m6 6 18 12"/></svg>`;

  // Data
  const heroImages = [
    "/generated/image-person-sitting-peacefully-by-a-window-wi-1765492123925-0.webp",
    "/generated/image-young-person-meditating-in-a-minimalist--1765492126375-1.webp",
    "/generated/image-person-journaling-at-a-cozy-desk-focused-1765492128866-2.webp",
    "/generated/image-person-walking-in-nature-peaceful-and-co-1765492131218-3.webp",
    "/generated/image-person-doing-gentle-yoga-at-home-calm-at-1765492133907-4.webp",
    "/generated/image-person-reading-a-book-in-a-comfortable-c-1765492136093-5.webp"
  ];

  const benefitCards = [
    {
      title: "Real-time emotional guidance.",
      desc: "Mirror recognizes your emotional patterns as they happen and guides you through AI-powered neuroplasticity techniques.",
      image: "/generated/image-person-using-their-phone-mindfully-sitti-1765492140691-6.webp"
    },
    {
      title: "Address triggers instantly.",
      desc: "When anxiety strikes, Mirror helps you rewire your response in the moment, building lasting emotional resilience.",
      image: "/generated/image-person-experiencing-a-moment-of-relief-a-1765492142922-7.webp"
    },
    {
      title: "Lasting emotional control.",
      desc: "Beyond temporary relief, Mirror creates permanent changes in how you respond to stress and anxiety.",
      image: "/generated/image-person-smiling-confidently-in-everyday-s-1765492145142-8.webp"
    }
  ];

  const steps = [
    {
      step: 1,
      title: "Share what you're feeling.",
      desc: "When anxiety or emotional overwhelm hits, open Mirror and describe what's happening. Our AI recognizes the pattern instantly.",
      image: "feeling"
    },
    {
      step: 2,
      title: "Get guided through the moment.",
      desc: "Mirror provides real-time neuroplasticity exercises tailored to your specific trigger, helping you rewire your emotional response.",
      image: "guided"
    },
    {
      step: 3,
      title: "Track your emotional patterns.",
      desc: "See how your triggers evolve over time. Mirror learns what works for you and adapts its guidance to your unique emotional landscape.",
      image: "track"
    },
    {
      step: 4,
      title: "Build lasting resilience.",
      desc: "With consistent practice, Mirror helps you create permanent changes in how you respond to stress, anxiety, and emotional triggers.",
      image: "resilience"
    }
  ];

  const faqs = [
    "How is Mirror different from meditation apps?",
    "Is Mirror a replacement for therapy?",
    "How quickly will I see results?",
    "What if I'm already on medication for anxiety?",
    "How does the AI understand my emotional patterns?"
  ];
</script>

<Header />

<main class="w-full overflow-x-hidden">
  <!-- Hero Section -->
  <section class="pt-32 pb-16 md:pt-40 md:pb-24 px-6 text-center max-w-7xl mx-auto">
    <h1 class="text-4xl md:text-6xl lg:text-7xl font-medium tracking-tight text-[#1A1A1A] mb-6 leading-[1.1]">
      Rewire anxiety.<br />Reclaim control.
    </h1>
    <p class="text-gray-600 text-lg md:text-xl max-w-3xl mx-auto mb-10 leading-relaxed font-light">
      AI-guided neuroplasticity that addresses emotional triggers in real time. When meditation and therapy haven't worked, Mirror helps you build lasting emotional resilience.
    </p>
    <button class="bg-[#1A1A1A] text-white px-8 py-3.5 rounded-sm font-medium hover:bg-black transition-colors">
      Start your journey
    </button>
  </section>

  <!-- Hero Images Scroll -->
  <div class="w-full overflow-x-auto pb-12 hide-scrollbar">
    <div class="flex gap-4 px-6 min-w-max">
      {#each heroImages as img, i}
        <div class="relative w-48 h-64 md:w-64 md:h-80 rounded-3xl overflow-hidden flex-shrink-0">
          <img src={img} alt="Lifestyle" class="w-full h-full object-cover" />
        </div>
      {/each}
    </div>
  </div>

  <!-- App Feature Section -->
  <section class="py-20 px-6 max-w-7xl mx-auto">
    <div class="bg-white rounded-[40px] p-8 md:p-16 flex flex-col md:flex-row items-center gap-12 shadow-sm">
      <!-- Phone Mockup -->
      <div class="w-full md:w-1/2 flex justify-center">
        <div class="relative w-[280px] h-[580px] bg-black rounded-[40px] border-[8px] border-black shadow-2xl overflow-hidden">
          <div class="absolute top-0 left-0 right-0 h-6 bg-black z-20 flex justify-center">
            <div class="w-20 h-4 bg-black rounded-b-xl"></div>
          </div>
          <div class="w-full h-full bg-white pt-10 px-4 overflow-hidden flex flex-col">
            <!-- Mock UI -->
            <div class="flex justify-between items-center mb-6">
              <div class="w-8 h-8 rounded-full bg-gray-200"></div>
              <div class="w-8 h-8 rounded-full bg-gray-100"></div>
            </div>
            <div class="mb-6">
              <div class="text-xs text-gray-500 mb-1">Today</div>
              <div class="text-2xl font-bold">Your Patterns</div>
            </div>
            <div class="space-y-3">
              <div class="h-20 bg-gray-50 rounded-xl w-full border border-gray-100 p-3">
                <div class="text-[10px] text-gray-600 mb-2">Work stress</div>
                <div class="w-full h-1.5 bg-primary-400 rounded"></div>
              </div>
              <div class="h-20 bg-gray-50 rounded-xl w-full border border-gray-100 p-3">
                <div class="text-[10px] text-gray-600 mb-2">Social anxiety</div>
                <div class="w-3/4 h-1.5 bg-primary-300 rounded"></div>
              </div>
              <div class="h-20 bg-gray-50 rounded-xl w-full border border-gray-100 p-3">
                <div class="text-[10px] text-gray-600 mb-2">Morning worry</div>
                <div class="w-1/2 h-1.5 bg-primary-500 rounded"></div>
              </div>
            </div>
          </div>
        </div>
      </div>
      
      <!-- Content -->
      <div class="w-full md:w-1/2 space-y-8">
        <h2 class="text-3xl md:text-4xl font-medium leading-tight text-[#1A1A1A]">
          Your emotions, understood.<br />
          Track emotional patterns, identify triggers, and see your progress over time. Mirror's AI learns what works for you and adapts its guidance to help you build lasting emotional control.
        </h2>
        <div class="flex items-center justify-between pt-4">
          <button class="flex items-center gap-2 text-[#1A1A1A] font-medium hover:opacity-70 transition-opacity">
            {@html PlayCircle}
            See how it works
          </button>
          <div class="flex gap-2">
            <button class="p-2 rounded-full border border-gray-200 hover:bg-gray-50 text-gray-400 hover:text-black transition-colors">
              {@html ChevronLeft}
            </button>
            <button class="p-2 rounded-full border border-gray-200 hover:bg-gray-50 text-gray-400 hover:text-black transition-colors">
              {@html ChevronRight}
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Value Proposition -->
  <section class="py-16 px-6 max-w-7xl mx-auto">
    <div class="grid md:grid-cols-2 gap-12 items-start">
      <h2 class="text-3xl md:text-5xl font-medium tracking-tight text-[#1A1A1A] leading-tight">
        You deserve to feel in control of your emotions.
      </h2>
      <p class="text-gray-600 text-lg font-light leading-relaxed">
        Anxiety doesn't have to define your life. When traditional approaches haven't worked, Mirror offers a different path—one based on neuroplasticity and real-time emotional guidance. You have the power to rewire your responses and build the emotional resilience you've been searching for.
      </p>
    </div>
  </section>

  <!-- Benefit Cards -->
  <section class="py-8 px-6 max-w-7xl mx-auto">
    <div class="grid md:grid-cols-3 gap-6">
      {#each benefitCards as card}
        <div class="relative h-[480px] rounded-3xl overflow-hidden group">
          <img src={card.image} alt={card.title} class="absolute inset-0 w-full h-full object-cover transition-transform duration-700 group-hover:scale-105" />
          <div class="absolute inset-0 bg-gradient-to-t from-black/60 via-black/20 to-transparent"></div>
          <div class="absolute bottom-0 left-0 right-0 p-8 text-white">
            <h3 class="text-2xl font-medium mb-3">{card.title}</h3>
            <p class="text-white/80 text-sm leading-relaxed font-light">{card.desc}</p>
          </div>
        </div>
      {/each}
    </div>
  </section>

  <!-- Testimonial -->
  <section class="py-24 px-6 max-w-4xl mx-auto text-center">
    <blockquote class="text-2xl md:text-3xl font-medium leading-relaxed text-[#1A1A1A] mb-8">
      "After years of trying meditation apps and therapy, Mirror was the first thing that actually helped me manage my anxiety in real time. It's like having a guide in my pocket that knows exactly what I need in the moment."
    </blockquote>
    <div class="flex flex-col items-center gap-3">
      <img src="/generated/image-relatable-millennial-looking-directly-at-1765492147205-9.webp" alt="Mirror User" class="w-12 h-12 rounded-full object-cover" />
      <div class="text-center">
        <div class="font-medium text-sm">Sarah M.</div>
        <div class="text-gray-500 text-xs">Mirror User, 6 months</div>
      </div>
    </div>
  </section>

  <!-- Stats Grid -->
  <section class="py-12 px-6 max-w-7xl mx-auto border-t border-gray-200">
    <div class="grid md:grid-cols-3 gap-8 text-center md:text-left">
      <div>
        <h3 class="text-xl font-medium mb-2">Instant emotional support.</h3>
        <p class="text-gray-500 text-sm font-light">When anxiety hits, Mirror is there. Get real-time guidance the moment you need it most.</p>
      </div>
      <div>
        <h3 class="text-xl font-medium mb-2">AI that learns you.</h3>
        <p class="text-gray-500 text-sm font-light">Mirror recognizes your unique emotional patterns and adapts its approach to what works for you.</p>
      </div>
      <div>
        <h3 class="text-xl font-medium mb-2">Lasting change, not quick fixes.</h3>
        <p class="text-gray-500 text-sm font-light">Build permanent emotional resilience through neuroplasticity-based techniques that rewire your responses.</p>
      </div>
    </div>
  </section>

  <!-- How it works -->
  <section class="py-20 px-6 max-w-7xl mx-auto" id="how-it-works">
    <div class="mb-16 max-w-md">
      <h2 class="text-4xl font-medium mb-6">How it works.</h2>
      <p class="text-gray-600 font-light">Mirror uses AI-powered emotional pattern recognition to guide you through neuroplasticity exercises in real time. It's like having a personal emotional coach that's always available when you need it.</p>
    </div>

    <div class="space-y-6">
      {#each steps as step}
        <div class="bg-white rounded-[40px] p-8 md:p-12 flex flex-col items-center text-center max-w-2xl mx-auto shadow-sm">
          <div class="w-full text-left mb-8">
            <span class="inline-block w-8 h-8 rounded-full border border-gray-200 text-center leading-8 text-sm font-medium mb-4">{step.step}</span>
            <h3 class="text-2xl font-medium mb-3">{step.title}</h3>
            <p class="text-gray-500 font-light text-sm max-w-lg">{step.desc}</p>
          </div>
          
          <!-- Phone Mockup for Step -->
          <div class="relative w-[240px] h-[480px] bg-black rounded-[35px] border-[6px] border-black shadow-xl overflow-hidden mt-4">
             <div class="absolute top-0 left-0 right-0 h-5 bg-black z-20 flex justify-center">
                <div class="w-16 h-3 bg-black rounded-b-lg"></div>
             </div>
             <div class="w-full h-full bg-white pt-8 px-3 overflow-hidden">
                <!-- Dynamic Content based on step -->
                {#if step.image === 'feeling'}
                  <div class="space-y-3 mt-4">
                    <div class="p-3 border rounded-xl border-black bg-gray-50">
                      <div class="font-bold text-xs mb-1">How are you feeling?</div>
                      <div class="h-1 w-full bg-gray-200 rounded"></div>
                    </div>
                    <div class="p-3 border rounded-xl border-gray-200">
                       <div class="font-bold text-xs mb-1 text-gray-400">Essential</div>
                       <div class="h-1 w-full bg-gray-100 rounded"></div>
                    </div>
                  </div>
                {:else if step.image === 'guided'}
                   <div class="mt-4">
                     <div class="text-center font-bold mb-4">Breathing Exercise</div>
                     <div class="bg-gray-100 h-32 rounded-xl mb-3 flex items-center justify-center text-xs text-gray-400">Map View</div>
                     <button class="w-full bg-black text-white text-xs py-2 rounded-lg">Confirm</button>
                   </div>
                {:else if step.image === 'track'}
                   <div class="bg-black h-full -mx-3 -mt-8 pt-10 px-3 text-white">
                      <div class="text-center mb-6">
                        <div class="w-12 h-12 bg-gray-700 rounded-full mx-auto mb-2"></div>
                        <div class="text-sm font-bold">Your Triggers</div>
                      </div>
                      <div class="space-y-2">
                         <div class="bg-gray-800 p-2 rounded-lg h-10"></div>
                         <div class="bg-gray-800 p-2 rounded-lg h-10"></div>
                      </div>
                   </div>
                {:else if step.image === 'resilience'}
                   <div class="mt-4 space-y-3">
                      <div class="font-bold text-sm">Health Status</div>
                      <div class="text-[10px] text-gray-500 leading-relaxed">
                        You usually make smart choices for your health through regular exercise...
                      </div>
                      <div class="bg-gray-50 p-2 rounded text-[10px] text-gray-600">
                        Since your diet lacks enough fruits and vegetables...
                      </div>
                   </div>
                {:else}
                   <div class="mt-4 flex flex-col h-full">
                      <div class="flex-1">
                        <div class="bg-gray-100 p-2 rounded-lg rounded-tl-none text-[10px] mb-2 max-w-[80%]">
                          What benefits can I get by bringing ApoB closer to the optimal range?
                        </div>
                        <div class="bg-blue-50 p-2 rounded-lg rounded-tr-none text-[10px] ml-auto max-w-[80%]">
                          By lowering ApoB, you reduce the number of cholesterol-carrying particles...
                        </div>
                      </div>
                      <div class="h-10 border-t mt-2"></div>
                   </div>
                {/if}
             </div>
          </div>
        </div>
      {/each}
    </div>
  </section>

  <!-- Dark Cards Section -->
  <section class="py-8 px-6 max-w-7xl mx-auto">
    <div class="grid md:grid-cols-2 gap-6">
      <!-- AI Card -->
      <div class="bg-[#111] rounded-[40px] p-8 md:p-12 text-white min-h-[500px] flex flex-col relative overflow-hidden">
        <div class="relative z-10">
          <h3 class="text-sm font-medium text-gray-400 mb-2">Powered by advanced AI.</h3>
          <h2 class="text-2xl md:text-3xl font-medium max-w-xs">Real-time emotional pattern recognition that adapts to you.</h2>
        </div>
        <!-- Abstract Neural Network Visual -->
        <div class="absolute inset-0 flex items-center justify-center opacity-20 mt-20">
           <svg viewBox="0 0 200 100" class="w-full h-full text-primary-500 fill-current">
              <!-- Simplified neural network representation -->
              {#each Array(50) as _, i}
                <circle cx={Math.random() * 200} cy={Math.random() * 100} r={Math.random() * 2} />
              {/each}
           </svg>
        </div>
      </div>

      <!-- Privacy Card -->
      <div class="bg-[#111] rounded-[40px] p-8 md:p-12 text-white min-h-[500px] flex flex-col relative overflow-hidden">
        <div class="relative z-10">
          <h3 class="text-sm font-medium text-gray-400 mb-2">Your mental health is private.</h3>
          <h2 class="text-2xl md:text-3xl font-medium max-w-xs">End-to-end encryption protects your emotional journey.</h2>
        </div>
        <!-- Blurred Text Visual -->
        <div class="absolute inset-0 flex items-center justify-center mt-20 overflow-hidden">
           <div class="text-4xl font-mono text-gray-600 opacity-20 blur-sm select-none break-all p-8">
             Anxi|%e$9ty Trig|I7g/er Emot|&5n! Feel|?Pm_Lw
           </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Pricing Section -->
  <section class="py-24 px-6 max-w-7xl mx-auto" id="join">
    <div class="text-center mb-16">
      <h2 class="text-3xl md:text-4xl font-medium mb-4">Start building emotional resilience today.</h2>
      <p class="text-gray-500 font-light max-w-2xl mx-auto">Choose the plan that fits your journey. All plans include AI-guided neuroplasticity exercises, real-time emotional support, and pattern tracking.</p>
    </div>

    <div class="grid md:grid-cols-2 gap-6 max-w-4xl mx-auto">
      <!-- Monthly Plan -->
      <div class="bg-white rounded-[32px] p-8 flex flex-col">
        <div class="w-12 h-12 bg-gray-100 rounded-full mb-6"></div>
        <h3 class="text-2xl font-medium mb-1">Monthly</h3>
        <p class="text-sm text-gray-500 mb-6">Try Mirror risk-free.</p>
        <div class="mb-8">
          <span class="text-2xl font-medium">$19.99</span>
          <span class="text-gray-400 text-sm">/mo</span>
          <div class="text-[10px] text-gray-400 mt-1 font-medium">Cancel anytime.</div>
        </div>
        <ul class="space-y-4 mb-8 flex-1">
          <li class="flex items-start gap-3 text-sm text-gray-600 font-light">
            <span class="mt-0.5 text-black">{@html Check}</span>
            Unlimited AI-guided emotional support sessions.
          </li>
          <li class="flex items-start gap-3 text-sm text-gray-600 font-light">
            <span class="mt-0.5 text-black">{@html Check}</span>
            Real-time trigger recognition and neuroplasticity exercises.
          </li>
          <li class="flex items-start gap-3 text-sm text-gray-600 font-light">
            <span class="mt-0.5 text-black">{@html Check}</span>
            Track emotional patterns and progress over time.
          </li>
        </ul>
        <button class="w-full bg-[#1A1A1A] text-white py-3 rounded-sm font-medium hover:bg-black transition-colors">Start free trial</button>
      </div>

      <!-- Annual Plan -->
      <div class="bg-white rounded-[32px] p-8 flex flex-col relative overflow-hidden">
        <div class="absolute top-0 right-0 bg-primary-50 px-4 py-1 rounded-bl-xl text-xs font-medium text-primary-900">Save 40%</div>
        <div class="w-12 h-12 bg-primary-100 rounded-full mb-6"></div>
        <h3 class="text-2xl font-medium mb-1">Annual</h3>
        <p class="text-sm text-gray-500 mb-6">Best value for lasting change.</p>
        <div class="mb-8">
          <span class="text-2xl font-medium">$11.99</span>
          <span class="text-gray-400 text-sm">/mo</span>
          <div class="text-[10px] text-gray-400 mt-1 font-medium">Billed annually at $143.88</div>
        </div>
        <ul class="space-y-4 mb-8 flex-1">
          <li class="flex items-start gap-3 text-sm text-gray-600 font-light">
            <span class="mt-0.5 text-black">{@html Check}</span>
            Everything in Monthly, plus priority support.
          </li>
          <li class="flex items-start gap-3 text-sm text-gray-600 font-light">
            <span class="mt-0.5 text-black">{@html Check}</span>
            Advanced analytics and deeper pattern insights.
          </li>
          <li class="flex items-start gap-3 text-sm text-gray-600 font-light">
            <span class="mt-0.5 text-black">{@html Check}</span>
            Early access to new features and techniques.
          </li>
        </ul>
        <button class="w-full bg-[#1A1A1A] text-white py-3 rounded-sm font-medium hover:bg-black transition-colors">Start free trial</button>
      </div>
    </div>
  </section>

  <!-- FAQ -->
  <section class="py-20 px-6 max-w-3xl mx-auto" id="faq">
    <h2 class="text-3xl font-medium text-center mb-12">Your questions answered.</h2>
    <div class="space-y-4">
      {#each faqs as question}
        <div class="border-b border-gray-200 py-4 flex justify-between items-center cursor-pointer group hover:bg-gray-50/50 transition-colors px-2">
          <span class="text-sm md:text-base font-medium text-gray-800">{question}</span>
          <span class="text-gray-400 group-hover:text-black transition-colors">{@html Plus}</span>
        </div>
      {/each}
    </div>
    <div class="mt-12 text-center">
      <button class="border border-gray-300 px-6 py-3 rounded-sm text-xs font-medium hover:bg-gray-50 transition-colors">
        View all Frequently Asked Questions
      </button>
    </div>
  </section>

  <!-- Footer -->
  <footer class="py-16 px-6 border-t border-gray-200 bg-[#F9F8F6]">
    <div class="max-w-7xl mx-auto">
      <div class="flex flex-col md:flex-row justify-between items-start md:items-center gap-8 mb-16">
        <a href="/" class="flex items-center gap-2">
           <span class="font-bold text-lg tracking-tight">Mirror</span>
        </a>
        
        <nav class="flex flex-wrap gap-6 md:gap-8 text-xs font-medium text-gray-600">
          <a href="#how-it-works" class="hover:text-black">How it works</a>
          <a href="#faq" class="hover:text-black">FAQ</a>
          <a href="#" class="hover:text-black">Blog</a>
          <a href="#" class="hover:text-black">Terms & Conditions</a>
          <a href="#" class="hover:text-black">Privacy Policy</a>
        </nav>

        <div class="flex gap-4 text-gray-800">
          <a href="#" class="hover:text-black">{@html XIcon}</a>
          <a href="#" class="hover:text-black">{@html Instagram}</a>
          <a href="#" class="hover:text-black">{@html LinkedIn}</a>
        </div>
      </div>

      <div class="text-[10px] text-gray-400 leading-relaxed max-w-5xl">
        <p class="mb-2">Mirror is a wellness technology platform designed to support emotional well-being through AI-guided techniques. Mirror is not a substitute for professional medical advice, diagnosis, or treatment. If you are experiencing a mental health crisis or emergency, please contact your local emergency services or a mental health crisis hotline immediately. Always seek the advice of qualified health providers with any questions you may have regarding a medical or mental health condition.</p>
        <p>The techniques and guidance provided by Mirror are based on neuroplasticity principles and are intended for educational and self-help purposes. Individual results may vary. Mirror does not guarantee specific outcomes or claim to cure, treat, or diagnose any medical or mental health condition.</p>
        <p class="mt-2">By using Mirror, you agree to our Terms of Service and Privacy Policy. Your emotional health data is encrypted and private. We never share your personal information without your explicit consent.</p>
      </div>
    </div>
  </footer>
</main>

<style>
  :global(body) {
    background-color: #F9F8F6;
    font-family: 'Inter', sans-serif;
  }
  
  .hide-scrollbar::-webkit-scrollbar {
    display: none;
  }
  .hide-scrollbar {
    -ms-overflow-style: none;
    scrollbar-width: none;
  }
</style>

