
<script setup>
    const propos = defineProps(['cadastraTarefa', 'tarefaTemp', 'trocaFiltro', 'editaTarefaTemp'])
</script>

<template>
<form @submit.prevent ="propos.cadastraTarefa">
    <div class="row">
    <div class="col">
        <input :value="propos.tarefaTemp" @change=" propos.editaTarefaTemp " required 
        type="text" placeholder="Digite aqui a descrição da tarefa" class="form-control">
    </div>
    <div class="col-md-2">
        <button type="submit" class="btn btn-primary">Cadastrar</button>
    </div>
    <div class="col-md-2">
    <div class="col-md-2">
        <select @change="propos.trocaFiltro" class="form-control">
            <option value="todas">Todas tarefas</option>
            <option value="pendentes">Pendentes</option>
            <option value="finalizadas">Finalizadas</option>
        </select>
    </div>
    </div>
    </div>
</form>
</template>