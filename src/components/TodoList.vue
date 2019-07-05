<template>
    <div class="mt-10" >
        <todo v-for="(todo, index) in todos" v-bind:todo="todo" v-bind:key="index" v-on:delete-todo="deleteTodo" v-on:complete-todo="completeTodo" ></todo>
    </div>
</template>
<script>

import Todo from './Todo';


export default {
    props: ['todos'],
    components : {
        Todo,
    },
    methods : {
        deleteTodo(todo){
            const todoIndex = this.todos.indexOf(todo);
            this.todos.splice(todoIndex, 1);
        },
        completeTodo(todo){
            const todoIndex = this.todos.indexOf(todo);
            this.todos[todoIndex].done = true;
        }
    }
};
</script>
<style>

.mt-10{
    margin-top: 10px;
}

</style>
