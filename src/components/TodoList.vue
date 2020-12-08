<template>
  <div>
    <button v-on:click="addTodo">ADD</button>
    <h5>TodoList</h5>
    <ul class="todolist">
      <li v-for="(todo, index) in todos" v-bind:key="index">
        {{ todo }}
        <button v-on:click="deleteTodo(index)">DEL</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      todos: []
    };
  },
  created() {
    this.todos = JSON.parse(localStorage.getItem("todos")) || [];
  },
  methods: {
    deleteTodo(index) {
      // ToDo削除
      this.todos.splice(index, 1);
      localStorage.setItem("todos", JSON.stringify(this.todos));
    },
    addTodo() {
      this.$router.push("/todos/add");
    }
  }
};
</script>

<style>
.todolist {
  list-style: none;
}
.todolist li {
  padding: 5px 0;
  vertical-align: center;
  position: relative;
}
</style>
