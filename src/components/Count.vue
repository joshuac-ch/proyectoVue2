<template>
<div class="contenedor">
  <h1>Contador {{ contador }}</h1>
  <br>
  <button type="button" class="verde" @click="incre">Incrementar</button>
  <button type="button" class="rojo" @click="decre">Decrementar</button>
</div>
</template>
<script setup>

import { ref } from 'vue'
const contador=ref(0)
const incre=()=>{
  contador.value++
}
const decre=()=>{
  contador.value--
}
</script>
<style>
.contenedor{
  .verde{
    cursor: pointer;
    border: 2px solid white;
    padding: 5px 20px;
    border-radius: 10px;
    margin: 10px;
    box-shadow: 0px 0px 50px 1px green;
  }
  .rojo{
    cursor: pointer;
    border: 2px solid white;
    padding: 5px 20px;
    border-radius: 10px;
    margin: 10px;
    box-shadow: 0px 0px 50px 1px red;
  }
}
</style>
