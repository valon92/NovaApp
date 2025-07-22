<template>
  <nav class="bg-gradient-to-r from-blue-600 via-purple-600 to-pink-600 p-4 shadow-lg">
    <div class="container mx-auto flex justify-between items-center">
      <a href="/" class="text-white text-3xl font-bold tracking-wider">NovaApp</a>

      <div class="hidden md:flex items-center space-x-4">
        <div class="relative">
          <input
            type="text"
            placeholder="Search..."
            class="py-2 pl-10 pr-4 rounded-full bg-white bg-opacity-20 text-white placeholder-white focus:outline-none focus:ring-2 focus:ring-white focus:bg-opacity-30 transition duration-300"
          />
          <svg
            class="absolute left-3 top-1/2 transform -translate-y-1/2 text-white"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
            width="20"
            height="20"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
            ></path>
          </svg>
        </div>
        <router-link
          to="/"
          class="text-white text-lg font-medium hover:text-gray-200 transition duration-300"
          >Home</router-link
        >
        <router-link
          to="/about"
          class="text-white text-lg font-medium hover:text-gray-200 transition duration-300"
          >About</router-link
        >
        <router-link
          to="/services"
          class="text-white text-lg font-medium hover:text-gray-200 transition duration-300"
          >Services</router-link
        >
        <router-link
          to="/contact"
          class="text-white text-lg font-medium hover:text-gray-200 transition duration-300"
          >Contact</router-link
        >
      </div>

      <div class="md:hidden flex items-center">
        <button @click="toggleMobileMenu" class="text-white focus:outline-none">
          <svg
            class="w-8 h-8"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              v-if="!mobileMenuOpen"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h16m-7 6h7"
            ></path>
            <path
              v-else
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M6 18L18 6M6 6l12 12"
            ></path>
          </svg>
        </button>
      </div>
    </div>

    <transition name="slide-down">
      <div
        v-if="mobileMenuOpen"
        class="md:hidden bg-gradient-to-r from-blue-700 via-purple-700 to-pink-700 mt-4 py-4 rounded-b-lg shadow-lg"
      >
        <div class="px-4 pb-4">
          <div class="relative mb-4">
            <input
              type="text"
              placeholder="Search..."
              class="w-full py-2 pl-10 pr-4 rounded-full bg-white bg-opacity-20 text-white placeholder-white focus:outline-none focus:ring-2 focus:ring-white focus:bg-opacity-30 transition duration-300"
            />
            <svg
              class="absolute left-3 top-1/2 transform -translate-y-1/2 text-white"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg"
              width="20"
              height="20"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
              ></path>
            </svg>
          </div>
          <router-link
            to="/"
            @click="closeMobileMenu"
            class="block text-white text-lg py-2 px-4 hover:bg-white hover:bg-opacity-10 rounded transition duration-300"
            >Home</router-link
          >
          <router-link
            to="/about"
            @click="closeMobileMenu"
            class="block text-white text-lg py-2 px-4 hover:bg-white hover:bg-opacity-10 rounded transition duration-300"
            >About</router-link
          >
          <router-link
            to="/services"
            @click="closeMobileMenu"
            class="block text-white text-lg py-2 px-4 hover:bg-white hover:bg-opacity-10 rounded transition duration-300"
            >Services</router-link
          >
          <router-link
            to="/contact"
            @click="closeMobileMenu"
            class="block text-white text-lg py-2 px-4 hover:bg-white hover:bg-opacity-10 rounded transition duration-300"
            >Contact</router-link
          >
        </div>
      </div>
    </transition>
  </nav>
</template>
  
  <script>
export default {
  name: 'NovaNavbar',
  data() {
    return {
      mobileMenuOpen: false,
    }
  },
  methods: {
    toggleMobileMenu() {
      this.mobileMenuOpen = !this.mobileMenuOpen
    },
    closeMobileMenu() {
      this.mobileMenuOpen = false
    },
  },
}
</script>
  
  <style scoped>
/* Transition styles for mobile menu */
.slide-down-enter-active,
.slide-down-leave-active {
  transition: all 0.3s ease-in-out;
  max-height: 500px; /* Adjust as needed */
  overflow: hidden;
}

.slide-down-enter-from,
.slide-down-leave-to {
  max-height: 0;
  opacity: 0;
}
</style>