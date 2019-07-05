<template>
  <div id="app">
    <todo-list v-bind:todos="todos"></todo-list>

    <create-todo v-on:create-todo="addTodo"></create-todo>
  </div>
</template>

<script>
import TodoList from "./components/TodoList";
import CreateTodo from "./components/CreateTodo";

export default {
  name: "App",
  components: {
    TodoList,
    CreateTodo
  },

  data() {
    return {
      todos: [
        {
          title: "title 1",
          project: "project 1",
          done: false
        },
        {
          title: "title 2",
          project: "project 2",
          done: true
        },
        {
          title: "title 3",
          project: "project 3",
          done: false
        },
        {
          title: "title 4",
          project: "project 4",
          done: false
        },
        {
          title: "title 5",
          project: "project 5",
          done: true
        },
        {
          title: "title 6",
          project: "project 6",
          done: false
        },
        {
          title: "title 7",
          project: "project 7",
          done: false
        },
        {
          title: "title 8",
          project: "project 8",
          done: false,
        },
      ],
    };
  },
  methods: {
    addTodo(newTodo) {
      console.log(newTodo);
      this.todos.push(newTodo);
    },
  },
};
</script>

<style>
</style>
