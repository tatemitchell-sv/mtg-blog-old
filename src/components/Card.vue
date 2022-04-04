<script setup lang="ts">
    defineProps ({
        source: String
    })
</script>

<template>
  <img :src="source" />
</template>

<style scoped>
    /* img {
        border-radius: 12px;
        width: 100%;
        height: auto;
        box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
    } */
</style>