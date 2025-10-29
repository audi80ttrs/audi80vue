<template>
  <div class="task-card">
    <h3>{{ task.title }}</h3>
    <p>{{ task.text }}</p>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  task: {
    id: number;
    title: string;
    text: string;
  };
}>();
</script>

<style scoped>
.task-card {
  border: 1px solid #ffffff;
  padding: 20px;
  margin-bottom: 18px;
  border-radius: 6px;
  background-color: #000000;
}
</style>