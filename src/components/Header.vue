<template>
  <header>
    <h1>{{ title }}</h1>
    <Button
      @btn-click="$emit('btn-click')"
      :text="showAddTaskBtn ? 'Close' : 'Add Task'"
      :icon="showAddTaskBtn ? 'fa fa-angle-up' : 'fa fa-angle-down'"
      :color="showAddTaskBtn ? 'red' : 'green'"
    />
  </header>
</template>

<script>
import Button from "./Button";
export default {
  name: "Header",
  props: {
    title: String,
    showAddTaskBtn: Boolean,
  },
  components: {
    Button,
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
