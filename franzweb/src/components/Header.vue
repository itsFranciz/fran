<script setup>
import franz_logo from '../assets/logo.png';
import { ref } from 'vue';

const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};
</script>

<template>
<nav class="sticky top-0 bg-black shadow-lg border-b-4 border-blue-500" style="z-index: 1000;">
  <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto mb-0 xl:px-0 container">

    <router-link to="/" class="flex items-center space-x-3 rtl:space-x-reverse">
      <img :src="franz_logo" class="h-20" alt="Franciz Logo" />
    </router-link>
    
    <button 
      @click="toggleMenu" 
      type="button" 
      class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200"
      aria-controls="navbar-solid-bg"
      aria-expanded="false"
    >
      <span class="sr-only">Open main menu</span>
      <svg class="w-5 h-5" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 17 14">
        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 1h15M1 7h15M1 13h15"/>
      </svg>
    </button>

    <div :class="{'hidden': !isMenuOpen, 'block': isMenuOpen}" class="w-full md:block md:w-auto b-5" id="navbar-solid-bg">
      <ul class="flex flex-col font-medium font-Rubik text-base mt-4 rounded-lg bg-black md:space-x-8 rtl:space-x-reverse md:flex-row md:mt-0 md:border-0 md:bg-transparent gap-7 md:mx-4">
          <li>
          <router-link to="/about" class="transition ease-in-out delay-150 duration-300 block py-2 px-3 md:p-0 text-white hover:text-blue-500 hover:scale-110 rounded"
          >
            ABOUT
          </router-link>
        </li>
        <li>
          <router-link to="/projects" class="transition ease-in-out delay-150 duration-300 block py-2 px-3 md:p-0 text-white hover:text-blue-500 hover:scale-110 rounded">
            PROJECTS
          </router-link>
        </li>
        <router-link to="/contact" class="transition ease-in-out delay-150 duration-300 block py-2 px-3 md:p-0 text-white hover:text-blue-500 hover:scale-110 rounded">
            CONTACT
          </router-link>
     
      </ul>
    </div>
  </div>
</nav>
</template>
