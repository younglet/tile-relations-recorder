<template>
{{ id }}
<div class="m-12">
    <div class="flex flex-col items-center justify-center">
        <div class="flex items-center">
            <Item class="w-36 h-36"/>
        </div>
        <div class="flex items-center justify-center">
            <Item class="w-36 h-36"/>
            <img :src="`/tiles/${id}.png`" class="size-36" >
            <Item class="w-36 h-36"/>
        </div>
        <div class="flex items-center">
            <Item class="w-36 h-36"/>
        </div>
    </div>
</div>

</template>

<script setup>
const route = useRoute()
const id = route.params.id
const directions = ['nw', 'n', 'ne', 'w', '', 'e', 'sw', 's', 'se']
</script>