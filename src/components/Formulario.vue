<script setup>
    const props = defineProps(['cadastraTarefa', 'tarefaTemp', 'trocarFiltro', 'editaTarefaTemp'])
</script>

<template>
    <form @submit.prevent="props.cadastraTarefa">
        <div class="row">
            <div class="col">
                <input :value="props.tarefaTemp" required class="form-control" type="text" placeholder="Digite aqui a descrição da tarefa..." @change="props.editaTarefaTemp">
            </div>
            <div class="col-md-1">
                <button class="btn btn-primary" type="submit">Cadastrar</button>
            </div>
            <div class="col-md-2">
            <select @change="props.trocarFiltro" class="form-control" name="" id="">
                <option value="todas">Todas tarefas</option>
                <option value="pendentes">Pendentes</option>
                <option value="finalizadas">Finalizadas</option>
            </select>
            </div>
        </div>
    </form>
</template>