<template>
  <div class="flex items-center justify-center min-h-screen bg-gray-100">
    <div class="bg-white rounded-xl shadow-lg p-10 flex flex-col items-center">
      <div class="text-6xl font-bold mb-8 text-gray-800">{{ counter }}</div>
      <div class="flex space-x-6">
        <button
          @click="decrement"
          class="px-6 py-3 text-lg font-semibold rounded-lg bg-red-500 text-white hover:bg-red-600 transition"
        >
          -
        </button>
        <button
          @click="increment"
          class="px-6 py-3 text-lg font-semibold rounded-lg bg-green-500 text-white hover:bg-green-600 transition"
        >
          +
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const counter = ref(0)

function increment() {
  counter.value++
}
function decrement() {
  counter.value--
}
</script>