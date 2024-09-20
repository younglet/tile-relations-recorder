<template>
    <div class=" w-auto h-auto flex flex-col justify-around border-2 relative" :class="borderColor">
        <div class="w-full h-full bg-violet-300 static"></div>
        <div class="p-4 w-full">
            <input type="range" min="0" max="2" step="1" v-model="value">
        </div>
    </div>
</template>

<script setup>
const value = ref(0)

const borderColor = computed(()=> {
    if (value.value === 0) return 'border-red-500'
    else if (value.value === 1) return 'border-orange-500'
    else return 'border-green-500'
})
</script>