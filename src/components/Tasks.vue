<template>
  <div :key="task.id" v-for="task in tasks">
    <TaskItem
      @toogle-reminder="$emit('toogle-reminder', task.id)"
      @delete-task="$emit('delete-task', task.id)"
      :task="task"
    />
  </div>
</template>

<script>
import TaskItem from "./Task";

export default {
  name: "TaskItems",
  components: {
    TaskItem,
  },
  props: {
    tasks: Array,
  },
  emits: ["delete-task", "toogle-reminder"],
};
</script>
