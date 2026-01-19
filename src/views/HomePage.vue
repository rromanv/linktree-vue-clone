<script setup>
import { ref } from 'vue'
import LinkCard from '@/components/LinkCard.vue'

const profile = ref({
  name: 'Rodolfo Roman',
  slogan: 'Full Stack Developer and Teacher',
  avatar:
    'https://api.dicebear.com/9.x/avataaars/svg?seed=Jack&accessories=sunglasses&accessoriesColor=25557c&accessoriesProbability=90&clothesColor=25557c&clothing=hoodie&clothingGraphic=pizza&eyebrows=defaultNatural&eyes=default&facialHair[]&facialHairColor[]&facialHairProbability=0&hairColor=4a312c&hatColor[]&mouth=twinkle&skinColor=edb98a&top=shortFlat&backgroundColor=c0aede',
})
</script>

<template>
  <main class="flex min-h-screen flex-col items-center px-4 py-8">
    <!-- Profile Header -->
    <div class="mb-8 flex flex-col items-center text-center">
      <div
        class="mb-4 h-24 w-24 overflow-hidden rounded-full border-4 border-green-400 shadow-lg shadow-green-500/20 sm:h-32 sm:w-32"
      >
        <img
          :src="profile.avatar"
          :alt="profile.name"
          class="h-full w-full object-cover"
        />
      </div>
      <h1 class="mb-2 font-display text-2xl font-bold text-white sm:text-3xl">
        {{ profile.name }}
      </h1>
      <p class="max-w-xs text-gray-300 sm:text-lg">{{ profile.slogan }}</p>
    </div>
  </main>
</template>
