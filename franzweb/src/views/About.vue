<script setup>
import Header from '@/components/Header.vue';
</script>

<template>
  <div class="max-h-[5000px] min-h-screen overflow-y-auto bg-black">
    <Header />

    <div class="container mx-auto justify-center mt-16">
      <h1 class="text-5xl font-bold text-center text-white font-serif mb-4">About Francis</h1>
      <p class="text-lg text-gray-600 text-center">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius corporis blanditiis amet aut. <br />
        Vero aliquam voluptas nesciunt quae doloremque commodi aperiam aut ipsa deleniti quia blanditiis quidem, a non eum?
      </p>
    </div>

    <div class="container mx-auto flex flex-col items-left space-y-10 mt-16">
      <div class="flex items-center space-x-4">
        <div class="bg-gray-800 rounded-full p-5 hover:scale-110 hover:rotate-6 transition-transform duration-300 ease-in-out">
          <i class="fa-brands fa-facebook text-[#1877F2] text-5xl hover:text-blue-400"></i>
        </div>
        <div class="flex flex-col">
          <h1 class="font-Rubik font-bold text-2xl text-blue-500">Facebook Gaming Page</h1>
        </div>
      </div>

      <div class="flex items-center space-x-4">
        <div class="bg-gray-800 rounded-full p-5 hover:scale-110 hover:rotate-6 transition-transform duration-300 ease-in-out">
          <i class="fa-brands fa-instagram text-pink-500 text-5xl hover:text-pink-400"></i>
        </div>
        <div class="flex flex-col">
          <h1 class="font-Rubik font-bold text-2xl text-pink-500">Instagram</h1>
        </div>
      </div>
    </div>
  </div>
</template>
