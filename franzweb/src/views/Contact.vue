<script setup>
import Header from '@/components/Header.vue';
</script>

<template>
    <Header />
    <div class="max-h-[5000px] min-h-screen overflow-y-auto bg-black flex flex-col items-center">  
      <div class="mx-auto text-center mt-16">
        <h1 class="text-5xl font-bold text-white font-serif mb-4">CONTACT</h1>
        <p class="text-lg text-gray-600">Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius corporis blanditiis amet aut. <br>
          Vero aliquam voluptas nesciunt quae doloremque commodi aperiam aut ipsa deleniti quia blanditiis quidem, a non eum?</p>
      </div>
  
      <!-- Form container -->
      <div class="bg-gray-900 py-7 rounded border border-blue-500 mt-16 mb-16 w-full max-w-4xl mx-auto">
        <form @submit="handleSubmit">
          <div class="px-4 sm:px-6 md:px-8">
            <h1 class="font-Quicksand text-3xl sm:text-4xl md:text-5xl text-white mb-6">Shoot me a message!</h1>
  
            <div v-if="successMessage" class="mb-5 text-green-500">{{ successMessage }}</div>
            <div v-if="errorMessage" class="mb-5 text-red-500">{{ errorMessage }}</div>
  
            <div class="mb-5">
              <label for="full-name" class="block mb-1 text-sm font-Rubik text-white">Full Name</label>
              <input type="text" id="full-name" v-model="fullName" class="border border-blue-500 bg-gray-800 text-white p-2 w-full rounded-md focus:ring-2 focus:ring-blue-500 placeholder:text-gray-400" placeholder="Full Name" required />
            </div>
  
            <div class="mb-5">
              <label for="phone" class="block mb-1 text-sm font-Rubik text-white">Contact Number</label>
              <input type="text" id="phone" v-model="phone" class="border border-blue-500 bg-gray-800 text-white p-2 w-full rounded-md focus:ring-2 focus:ring-blue-500 placeholder:text-gray-400" placeholder="Contact Number" required />
            </div>
  
            <div class="mb-5">
              <label for="email" class="block mb-1 text-sm font-Rubik text-white">Email</label>
              <input type="email" id="email" v-model="email" class="border border-blue-500 bg-gray-800 text-white p-2 w-full rounded-md focus:ring-2 focus:ring-blue-500 placeholder:text-gray-400" placeholder="Email" required />
            </div>
  
            <div class="mb-5">
              <label for="message" class="block mb-1 text-sm font-Rubik text-white">Message</label>
              <textarea id="message" v-model="message" rows="4" class="border border-blue-500 bg-gray-800 text-white p-2 w-full rounded-md focus:ring-2 focus:ring-blue-500 placeholder:text-gray-400" placeholder="Your message here..." required></textarea>
            </div>
  
            <button type="submit" :disabled="isSubmitting" class="bg-blue-500 p-2 w-full rounded-md text-sm text-white hover:bg-[#79a8df] transition-all duration-200">
              {{ isSubmitting ? 'Sending...' : 'Send' }}
            </button>
          </div>
        </form>
      </div>
  
    </div>
  </template>
  
