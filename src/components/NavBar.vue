<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'

const isScrolled = ref(false)

const handleScroll = () => {
  isScrolled.value = window.scrollY > 20
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})

const links = [
  { name: 'Methodology', href: '#methodology' },
  { name: 'Perspectives', href: '#perspectives' },
  { name: 'Impact', href: '#impact' },
  { name: 'GitHub', href: '#' },
]
</script>

<template>
  <nav 
    class="fixed top-0 left-0 right-0 z-50 transition-all duration-300 border-b"
    :class="[
      isScrolled 
        ? 'bg-white/80 backdrop-blur-md border-slate-200 py-3 shadow-sm' 
        : 'bg-transparent border-transparent py-5'
    ]"
  >
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex items-center justify-between">
      <!-- Logo -->
      <div class="flex items-center gap-3">
        <img 
          src="/genefoundry_logo.svg" 
          alt="GeneFoundry Logo" 
          class="h-10 w-10 drop-shadow-lg animate-float"
        />
        <span class="text-xl font-bold tracking-tight text-secondary">
          Gene<span class="text-primary">Foundry</span>
        </span>
      </div>

      <!-- Desktop Navigation -->
      <div class="hidden md:flex items-center gap-8">
        <a 
          v-for="link in links" 
          :key="link.name" 
          :href="link.href"
          class="text-sm font-medium text-slate-600 hover:text-primary transition-colors"
        >
          {{ link.name }}
        </a>
      </div>

      <!-- Mobile Menu Button (Placeholder) -->
      <button class="md:hidden text-slate-600">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="4" y1="12" x2="20" y2="12"/><line x1="4" y1="6" x2="20" y2="6"/><line x1="4" y1="18" x2="20" y2="18"/></svg>
      </button>
    </div>
  </nav>
</template>

<style scoped>
@keyframes float {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-3px); }
}
.animate-float {
  animation: float 3s ease-in-out infinite;
}
</style>
