<template>
  <div class="flex flex-col justify-center items-center gap-4  p-4">
    <div v-for="group in groups" :key="group" class="grid grid-cols-3 size-32 w-64 gap-4 border h-auto">
      <div v-for="tile in group" :key="tile">
        <NuxtLink :href="`/${tile}`"  class="flex flex-col items-center justify-center" >
          <img :src="`/tiles/${tile}.png`" class="size-12" />
          <h3>{{ tile }}</h3>
        </NuxtLink>
      </div>
    </div>
  </div>

</template>


<script setup>
const types = ['land', 'water']
const directions = ['nw', 'n', 'ne', 'w', '', 'e', 'sw', 's', 'se']
const groups = types.map(type => directions.map(direction => `${type}_${direction}`))
</script>