<script setup>
import { ref } from 'vue'
const task = ref([])
const inputTask = ref ('')
function addTask (){
    task.value.push(inputTask.value)
    console.log(task)
}
</script>

<template>
    <div class=" py-8 px-10 max-w-96 bg-slate-300 rounded shadow mx-auto mt-10 ">
        <h1 class=" text-center text-lg ">Lista de Tareas</h1>
        <div class="mt-4 mb-2">
            <input v-model="inputTask" class=" w-4/5 " />
            <button @click="addTask" class=" w-1/5 bg-green-600 text-white font-bold">+</button>
        </div>
        <div v-for="(task,index) in task" :key="index" class=" bg-white/60 px-2 mb-1">
            {{ task }}
        </div>
    </div>
</template>