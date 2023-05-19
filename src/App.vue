<script setup>
import { livros } from '@/_data/livros.js'
</script>

<template>
  <h1>Livros disponiveis</h1>
  <div class="listagem-livros">
    <div class="card-livro" v-for="livro in livros" :key="livro.id">
      <img :src="livro.img" alt="Capa do livro" class="capa-livro" />
      <p class="titulo-livro">Título: {{ livro.title }}</p>
      <p class="autor-livro">Autor: {{ livro.author }}</p>
      <p class="preco-livro">Preço: R${{ livro.price.toFixed(2) }}</p>
    </div>
  </div>
  <!-- {{ livros }} -->
</template>

<style scoped>
.listagem-livros {
  display: flex;
  flex-wrap: wrap;
}
.capa-livro {
  width: 200px;
}
.card-livro p {
  margin: 0;
}
.card-livro .titulo-livro {
  font-weight: bold;
  margin-bottom: 5px;
}
.card-livro {
  margin: 5px 10px;
  padding: 10px;
  background-color: beige;
  border-radius: 10px;
}
</style>