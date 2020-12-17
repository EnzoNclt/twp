<template>
  <div class="row mt-5">
    <div class="col-3">
      <div class="p-2 alert alert-secondary">
        <h3>To Do List</h3>
        <ul>
          <li v-for="todo in todos" :key="todo.id">
            {{ todo.task }}
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    todos() {
      return this.$store.getters.getTodos;
    },
  },
};
</script>

<style>
/* light stylings for the twp columns */
.twp-column {
  min-height: 300px;
}
</style>