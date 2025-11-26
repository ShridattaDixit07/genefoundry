<script setup lang="ts">
// Hero Section
</script>

<template>
  <section class="relative pt-32 pb-20 lg:pt-48 lg:pb-32 overflow-hidden bg-slate-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
      <div class="grid lg:grid-cols-2 gap-12 items-center">
        <!-- Text Content -->
        <div class="text-center lg:text-left">
          <h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold tracking-tight text-secondary mb-6 leading-tight">
            Forging Trust in <br/>
            <span class="text-primary">Genomic AI.</span>
          </h1>
          <p class="text-lg sm:text-xl text-slate-600 mb-8 max-w-2xl mx-auto lg:mx-0 leading-relaxed">
            A modular registry for customized, evidence-based genomic analysis. Powered by Model Context Protocols (MCPs).
          </p>
          <div class="flex flex-col sm:flex-row items-center justify-center lg:justify-start gap-4">
            <a href="#" class="px-8 py-3 bg-primary text-white rounded-full font-semibold hover:bg-pink-600 transition-all shadow-lg hover:shadow-primary/25 flex items-center gap-2">
              <span>Get Started on GitHub</span>
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M15 22v-4a4.8 4.8 0 0 0-1-3.5c3 6 2 7.8 2 12 0 1.7-.5 3-1.5 4-1 .9-2.5 1-4.5 1-3 0-4.5-1-5.5-2.5 0-.5 0-1 .5-1.5 1 1 1.5 2 2.5 2 2.5 0 5 1 4.5 2 4 2 1.5 0 2.5-.5 3-1.5.5-1 .5-2 .5-3.5a4.8 4.8 0 0 0-1-3.5c3-1.5 3.5-1.5 5-2.5s2-1.5 3-1.5 3.5 1.5 4.5 3.5 4.5 3.5 0 1 1 1.5 1 2.5 1 4.5 0 6 1.5 7 3 7 3 0 5 1 4.5 2 4 2 1.5 0 2.5-.5 3-1.5.5-1 .5-2 .5-3.5z"/></svg>
            </a>
          </div>
        </div>

        <!-- Visual: The Anvil & The Flow -->
        <div class="relative h-[400px] flex items-center justify-center select-none">
          <!-- The Flow (AI) - Ethereal, moving around the structure -->
          <div class="absolute w-72 h-72 bg-gradient-to-tr from-primary/30 to-purple-500/30 rounded-full blur-3xl animate-pulse-slow"></div>
          
          <!-- The Anvil (MCP Structure) - Solid, grounding -->
          <div class="relative z-10 w-72 bg-white/90 backdrop-blur-md rounded-xl shadow-2xl border border-slate-200 overflow-hidden transform -rotate-2 hover:rotate-0 transition-transform duration-500">
             <!-- Header -->
             <div class="bg-slate-50 px-4 py-3 border-b border-slate-100 flex items-center justify-between">
                <div class="flex items-center gap-2">
                   <div class="w-2.5 h-2.5 rounded-full bg-slate-300"></div>
                   <div class="w-2.5 h-2.5 rounded-full bg-slate-300"></div>
                </div>
                <div class="text-xs font-mono text-slate-400">mcp-server-gnomad</div>
             </div>
             <!-- Code/Content -->
             <div class="p-5 font-mono text-xs sm:text-sm text-slate-600 space-y-2">
                <div class="flex gap-2">
                   <span class="text-purple-500">source:</span>
                   <span class="text-green-600">"gnomAD v4.0"</span>
                </div>
                <div class="flex gap-2">
                   <span class="text-purple-500">gene:</span>
                   <span class="text-blue-600">"PKD1"</span>
                </div>
                <div class="flex gap-2">
                   <span class="text-purple-500">af_popmax:</span>
                   <span class="text-orange-500">0.000042</span>
                </div>
                <div class="flex gap-2">
                   <span class="text-purple-500">status:</span>
                   <span class="text-primary font-bold">"VERIFIED"</span>
                </div>
             </div>
          </div>
          
          <!-- Floating Data Particles -->
          <div class="absolute top-1/4 right-1/4 w-3 h-3 bg-primary rounded-full animate-float-delay-1"></div>
          <div class="absolute bottom-1/3 left-1/4 w-2 h-2 bg-slate-400 rounded-full animate-float-delay-2"></div>
          <div class="absolute top-1/3 left-10 w-4 h-4 bg-purple-400 rounded-full animate-float-delay-3 opacity-50"></div>
        </div>
      </div>
    </div>
    
    <!-- Background Elements -->
    <div class="absolute top-0 right-0 -translate-y-1/4 translate-x-1/4 w-96 h-96 bg-slate-200/50 rounded-full blur-3xl -z-10"></div>
    <div class="absolute bottom-0 left-0 translate-y-1/4 -translate-x-1/4 w-64 h-64 bg-primary/5 rounded-full blur-3xl -z-10"></div>
  </section>
</template>

<style scoped>
.animate-pulse-slow {
  animation: pulse 6s cubic-bezier(0.4, 0, 0.6, 1) infinite;
}
@keyframes pulse {
  0%, 100% { opacity: 0.4; transform: scale(1); }
  50% { opacity: 0.6; transform: scale(1.1); }
}

@keyframes float {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
}
.animate-float-delay-1 { animation: float 4s ease-in-out infinite; animation-delay: 0s; }
.animate-float-delay-2 { animation: float 5s ease-in-out infinite; animation-delay: 1s; }
.animate-float-delay-3 { animation: float 6s ease-in-out infinite; animation-delay: 2s; }
</style>
