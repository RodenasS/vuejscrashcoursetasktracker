<template>
  <header>
    <h1>{{ title }}</h1>
    <ButtonItem @btn-click="$emit('toggle-add-task')" :text="showAddTask ? 'Close' : 'Add Task'" :color="showAddTask ? 'red' : 'green'"> {{text}}></ButtonItem>
  </header>
</template>

<script>
import ButtonItem from "@/components/Button-Item";

export default {
  name: 'Header-Item',
  components: {ButtonItem},
  props: {
    title: String,
    showAddTask: Boolean,
  },
  component : {
    ButtonItem
  }
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>