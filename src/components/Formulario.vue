<script setup>
  const props = defineProps(['cadastraTarefa', 'tarefaTemp', 'trocarFiltro', 'editaTarefaTemp'])
</script>

<template>
    <form @submit.prevent="props.cadastraTarefa">
      <div class="row">
        <div class="col">
          <input :value="props.tarefaTemp" @change="props.editaTarefaTemp" required class="form-control" placeholder="Digite aqui a descrição da tarefa" type="text">
        </div>
        <div class="col-md-2">
          <button class="btn btn-primary" type="submit">cadastrar</button>
        </div>
        <div class="col-md-2">
          <select @change="props.trocarFiltro" class="form-control">
            <option value="todas">Todas tarefas</option>
            <option value="pendentes">pendentes</option>
            <option value="finalizadas">finalizadas</option>
          </select>
        </div>
      </div>
    </form>
</template>