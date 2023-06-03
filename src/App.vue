<template>
  <main>
    <div class="overlay" v-show="showModal">
      <div class="modal">
        <textarea name="note" id="note" cols="30" rows="10"></textarea>
        <button>Add Note</button>
        <button class="close" @click="showModal = false">Close</button>
      </div>
    </div>
    <div class="container">
      <header>
        <h1>Notes</h1>
        <button @click="showModal = true">+</button>
      </header>
      <div class="cards-container">
        <div class="card">
          <p class="main-text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Beatae, et.</p>
          <p class="date">10/10/23126</p>
        </div>
      </div>
    </div>
  </main>
</template>

<script setup>
import { ref } from 'vue';


const showModal = ref(false);
</script>

<style scoped>
main{
  height: 100vh;
  width: 100vw;
}
.container {
  max-width: 1000px;
  padding: 10px;
  margin: 0 auto;
}
header{
  display: flex;
  justify-content: space-between;
  align-items: center;
}
h1 {
  font-weight: bold;
  margin-bottom: 25px;
  font-size: 75px;
}
header button{
  border:none;
  padding: 10px;
  width: 50px;
  height: 50px;
  cursor: pointer;
  background-color: rgb(0, 0, 0);
  border-radius: 100%;
  color: white;
  font-size: 25px;
}
.card{
  width: 225px;
  height: 225px;
  background-color: rgb(179, 176, 7);
  padding: 10px;
  border-radius: 15px; 
  display: flex;
  flex-direction: column;
  margin-right: 20px;
  margin-bottom: 20px;
}
.date{
  font-size: 12.5px;
  font-weight: bold;
}
.cards-container{
  display: flex;
  flex-wrap: wrap;
}
.overlay{
  position: absolute;
  height: 100%;
  width: 100%;
  background-color: black;
  z-index: 10;
  display: flex;
  align-items: center;
  justify-content: center;
}
.modal{
  width: 750px;
  background-color: bisque;
  border-radius: 10px;
  padding: 30px;
  position: relative;
  display: flex;
  flex-direction: column;
}
.modal button {
  padding: 10px 20px;
  font-size: 20px;
  width: 100%;
  background-color: blueviolet;
  border: none;
  color: white;
  cursor: pointer;
  margin-top: 15px;
}
.modal .close{
  background-color: red;
  margin-top: 7px;
}
</style>