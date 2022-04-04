<script setup lang="ts">
import Card from './Card.vue'
import data from '../../data.json'
let filterData = data
const filter = event =>{
  console.log(event)
  filterData = data.filter(card => {
    return card.color?.includes("red")
  })
}

</script>

<template>
  <h1>G'day Cards</h1>
  <button @click="filter">Red</button>
  <div class="glide">
    <div class="glide__track" data-glide-el="track">
      <ul class="glide__slides">
        <li class="glide__slide" v-for="card in filterData" :key="i"><Card :source="card.source"></Card></li>
      </ul>
    </div>
    <div data-glide-el="controls">
    <button data-glide-dir="<<">Start</button>
    <button data-glide-dir="<">Previous</button>
    <button data-glide-dir=">">Next</button>
    <button data-glide-dir=">>">End</button>
  </div>
  </div>

</template>

<style scoped>
  /* ul {
    max-width: 100%;
    display: grid;
    grid-template-columns: auto auto auto auto auto;
    grid-gap: 25px;
    list-style-type: none;
  } */

</style>
