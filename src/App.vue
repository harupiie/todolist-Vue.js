<template>
  <div id="box">
    <h3>MyTodo</h3>
    <router-view></router-view>
  </div>
</template>

<script>
// import TodoForm from "./components/TodoForm";
// import TodoList from "./components/TodoList";

// export default {
//   components: {
//     "todo-form": TodoForm,
//     "todo-list": TodoList
//   }
// methods: {
//   addTodo(newTodo) {
//     // ToDo追加
//     this.todos.push(newTodo);
//     localStorage.setItem("todos", JSON.stringify(this.todos));
//   },
//   deleteTodo(index) {
//     // ToDo削除
//     this.todos.splice(index, 1);
//     localStorage.setItem("todos", JSON.stringify(this.todos));
//   }
// }
// };
</script>

<style>
#box {
  padding: 30px 30px;
}
</style>
