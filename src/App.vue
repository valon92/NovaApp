<template>
  <div>
    <Navbar />

    <HeroSection />
    <FeaturesSection />
    <ProjectGallery />
    <Footer />
  </div>
</template>

<script setup>
import HeroSection from './components/HeroSection.vue'
import FeaturesSection from './components/FeaturesSection.vue'
import ProjectGallery from './components/ProjectGallery.vue'
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'
</script>
