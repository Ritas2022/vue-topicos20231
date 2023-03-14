<script setup lang="ts">
import {ref}from 'vue';
const nome = ref("Nome");
const contador =ref(1)
function incrementar(){
  contador.value++
}

</script>


<template>
  <div class="about">
    <h1>Bem Vindo{{ nome }}</h1>
    <p><input type="text" v-model="nome"/></p>
    <p v-if="nome.length> 5">Nome longo</p>
    <p v-else>nome curto</p> 
   <p> {{contador}} <button @click="incrementar">Botão</button></p>
  </div>
</template>
