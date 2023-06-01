<template>
  <main>
    <div>
    <h4>The Current Count is...</h4>
    <h1>{{ count }}</h1>
    <button @click="count--">-</button>
    <button @click="count++">+</button>
  </div>
  </main>
  
</template>

<script setup>
import { ref } from 'vue';

  const count = ref(0);


</script>

<style scoped>
main {
  background-color: aquamarine;
  height: 100vh;
  width: 100vw;
  display: flex;
  align-items: center;
  justify-content: center;
}
div {
  text-align: center;
}
</style>