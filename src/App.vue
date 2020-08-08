<template>
  <div id="app">
    <Todos v-bind:todos="todos" />
    <TodoItem />
  </div>
</template>

<script>
import Todos from "./components/Todos";
import TodoItem from "./components/TodoItem";

export default {
  name: "App",
  components: {
    Todos,
    TodoItem,
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "Todo One",
          completed: false,
        },
        {
          id: 2,
          title: "Todo Two",
          completed: true,
        },
        {
          id: 3,
          title: "Todo Three",
          completed: false,
        },
      ],
    };
  },
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.4;
}
</style>
