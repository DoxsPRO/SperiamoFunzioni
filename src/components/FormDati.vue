<script setup>
//prossimo step unire tutti gli input e stamparli nel console log e vedere cosa ne esce fuori
import { ref } from 'vue'

const message = ref('') // dichiarazione corretta

function say() {
  console.log(message.value) // uso corretto di ref
}
</script>

<template>
  <div>
    <form @submit.prevent="say"> <!-- evitare il refresh -->
      <p>Add item</p>
      <p>Nome: <input type="text" v-model="message" placeholder="nome" required></p>
      <p>Cognome: <input type="text" placeholder="cognome" required></p>
      <p>Anni: <input type="date" required></p>
      <button type="submit">Add item</button>
    </form>
  </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
