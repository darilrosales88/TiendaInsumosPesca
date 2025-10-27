
<template>
  <h1>Estas aquí, este es el inicio!</h1>
  <p> la variable contador tiene valor {{contador}}</p>
  <p><button @click="incrementar">incrementar</button></p>
  <p><button @click="decrementar">decrementar</button></p> 
</template>
<script setup>
import { ref} from 'vue'; //para la utilizacion de variables reactivas
const contador =  ref(0) //iniciando una variable reactiva en valor 0
const incrementar = () => {
  contador.value++; //contador.value es la manera de acceder al valor de una variable reactiva
}

const decrementar = () => {
  contador.value--; //contador.value es la manera de acceder al valor de una variable reactiva
}

</script>

<style scoped>
p{
  color: red;
}
</style>