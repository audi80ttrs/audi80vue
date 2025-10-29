<template>
  <div>
    <h1>📋 Список дел</h1>
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
  { id: 1, title: 'Купить молоко', text: 'Не забыть в магазине' },
  { id: 2, title: 'Сделать уборку', text: 'Пропылесосить и вытереть пыль' },
  { id: 3, title: 'Изучить Vue', text: 'Пройти курс по Vue 3 и TypeScript' },
  { id: 4, title: 'Купить молоко', text: 'Не забыть варлваоыраловыр магазине' },
]);
</script>

<style>
body {
  font-family: Arial, sans-serif;
  padding: 20px;
}
</style>