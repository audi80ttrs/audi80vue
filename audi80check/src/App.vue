<template>
  <div>
    <h1>🧾 Список дел на счет AUDI</h1>
    <TaskItem
      v-for="task in tasks"
      :key="task.id"
      :task="task"
    />
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import TaskItem from './components/TaskItem.vue';

interface Task {
  id: number;
  title: string;
  text: string;
}

const tasks = ref<Task[]>([
  { id: 1, title: 'Купить Audi 80 B3', text: 'Необязательно cвап мотор' },
  { id: 2, title: 'Сделать ТО', text: 'Необязательно свап мотора' },
  { id: 3, title: 'Поставить на учет в ГАИ', text: 'Как поставят радоваться красивым номерам' },
  { id: 4, title: 'Починить и привести в отличное состояние', text: 'Поставить в гараж и задуматься о покупке другой Audi' },
  { id: 5, title: 'Купить Audi RS 6', text: 'Необязательно не разложиться' }
]);
</script>

<style>
body {
  font-family: Arial, sans-serif;
  padding: 14px;
}
</style>