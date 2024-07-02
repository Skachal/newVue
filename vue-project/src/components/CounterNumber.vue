<template>
  <div>
    <h2>Schot</h2>
    <h1 :style="{color: countColor}">{{ count }}</h1>
    <button @click="increment">Pribavit 1</button>
    <button @click="decrement">Otnat 1</button>
  </div>
</template>

<style scoped>
.h1 {
  color: aqua;
}
</style>

<script setup>
import { ref, computed } from 'vue'

const count = ref(0)

const increment = () => {
  count.value++
}

const decrement = () => {
  count.value--
}

const countColor = computed(() => {
  return count.value > 0 ? 'green' : count.value < 0 ? 'red' : 'black'
})
</script>
