<template>
  <header>
    <h1>Task Tracker</h1>
    <ButtonItem text="Add task" color="green" />
  </header>
</template>

<script>
import ButtonItem from "./Button";

export default {
  name: "HeaderItem",
  components: {
    ButtonItem,
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
