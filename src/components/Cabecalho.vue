
<script setup>
    const propos = defineProps(['tarefasPendentes'])
</script>

<template>
    <header class="p-5 mb-4 bg-light rounded-3">
        <h1>Minhas tarefas</h1>
        <p>
            Você possui {{ propos.tarefasPendentes }} tarefas pendentes
        </p>
    </header>
</template>
