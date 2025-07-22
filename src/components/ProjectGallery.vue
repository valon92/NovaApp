<template>
  <section class="bg-white py-16 px-6">
    <div class="max-w-6xl mx-auto text-center">
      <h2 class="text-3xl font-bold text-gray-900 mb-12">My Recent Projects</h2>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div
          v-for="(project, index) in projects"
          :key="index"
          class="bg-gray-100 rounded-xl shadow-md overflow-hidden hover:shadow-lg transition"
        >
          <img :src="project.image" alt="" class="w-full h-48 object-cover" />
          <div class="p-6">
            <h3 class="text-xl font-semibold text-gray-800 mb-2">{{ project.title }}</h3>
            <p class="text-gray-600">{{ project.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
  
  <script setup>
const projects = [
  {
    title: 'Vue Landing Page',
    description: 'A responsive landing page built with Vue.js and Tailwind CSS.',
    image: 'https://via.placeholder.com/400x200.png?text=Landing+Page',
  },
  {
    title: 'Admin Dashboard',
    description: 'A clean dashboard UI with Vue and Bootstrap.',
    image: 'https://via.placeholder.com/400x200.png?text=Dashboard',
  },
  {
    title: 'Portfolio Site',
    description: 'My personal portfolio showing skills and previous work.',
    image: 'https://via.placeholder.com/400x200.png?text=Portfolio',
  },
]
</script>
  