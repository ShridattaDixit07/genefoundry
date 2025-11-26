<script setup lang="ts">
import NavBar from './components/NavBar.vue'
import HeroSection from './components/HeroSection.vue'
import MethodologyFlow from './components/MethodologyFlow.vue'
import RoleSwitcher from './components/RoleSwitcher.vue'
import ImpactGrid from './components/ImpactGrid.vue'
import FooterSection from './components/FooterSection.vue'
</script>

<template>
  <div class="min-h-screen font-sans text-secondary bg-slate-50 selection:bg-primary/20 selection:text-primary">
    <NavBar />
    <main>
      <HeroSection />
      <MethodologyFlow />
      <RoleSwitcher />
      <ImpactGrid />
    </main>
    <FooterSection />
  </div>
</template>
