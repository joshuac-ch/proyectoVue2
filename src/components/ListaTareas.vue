<template>
<div class="contenedor2">
  <h2>Lista de Tareas</h2>
  <input type="text" v-model="tarea" @keyup.enter="addTask" placeholder="ingrese tarea">
  <div>
    <ul v-for="(t , i) in listatareas" :key="i">
      <li>{{ t }}</li>
    </ul>

  </div>
</div>
</template>
<script setup>
 import { ref } from 'vue';
 const listatareas=ref([])
 const tarea=ref("")
 const addTask=()=>{
  listatareas.value.push(tarea.value)
  tarea.value=""
 }
</script>

<style>
</style>
