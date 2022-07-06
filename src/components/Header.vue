<template>
  <header>
    <h1>Task Tracker</h1>
    <ButtonItem
      @btn-click="$emit('toogle-add-task')"
      :text="showAddTask ? 'Close' : 'Add Task'"
      :color="showAddTask ? 'red' : 'green'"
    />
  </header>
</template>

<script>
import ButtonItem from "./Button";

export default {
  name: "HeaderItem",
  components: {
    ButtonItem,
  },
  props: {
    showAddTask: Boolean,
  },
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
