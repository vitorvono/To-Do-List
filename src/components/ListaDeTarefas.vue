<script setup>
const props = defineProps(['tarefas'])

</script>


<template>
    <!-- criar um v-if se tarefas for < 0, exibir mensagem de que não há tarefas -->
    <ul class="list-group mt-4">
        <li class="list-group-item" v-for="tarefa in props.tarefas">
            <input @change="e => tarefa.finalizada = e.target.checked" :checked="tarefa.finalizada" type="checkbox"
                :id="tarefa.titulo">
            <label :class="{ done: tarefa.finalizada }" class="ms-3" :for="tarefa.titulo">{{ tarefa.titulo }}</label>
        </li>
    </ul>
</template>

<style scoped>
.done {
    text-decoration: line-through;
}
</style>
