<script setup>
import { ref} from 'vue'; //para la utilizacion de variables reactivas
import listaDeTareas from './components/listaDeTareas.vue';
import contador from './components/contador.vue';
</script>

<template>
  <contador></contador> 
  <listaDeTareas></listaDeTareas>
</template>

<style scoped>
p{
  color: red;
}
</style>
