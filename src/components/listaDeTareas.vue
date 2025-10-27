<template>
    <div>
     <h2>Lista de tareas</h2> 
     <input type="text" v-model="nuevaTarea" @keyup.enter="agregarTarea"><!-- v-model es una directiva de vue para cambiar de forma reactiva 
     el valor de esa variable,     es un intercambio bidireccional entre la variable declarada en el script y el campo del formulario,
     @keyup.enter es otra directiva donde      keyup es la directiva en si y enter es la tecla se dispara la ejecucion de la funcion 
     flecha agregarTarea -->
     <ul>
        <li v-for="(tarea,index) in tareas" :key="index">
            {{tarea}}
        </li>
     </ul>  
    </div>
    
</template> 

<script setup>
import { ref } from 'vue';

const tareas = ref([]);
const nuevaTarea = ref('');

const agregarTarea = () =>{
    tareas.value.push(nuevaTarea.value);
    nuevaTarea.value = '';
}
</script>

<style>

</style>