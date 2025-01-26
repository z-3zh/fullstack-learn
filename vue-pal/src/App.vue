<template>
  <div class="todo-list">
    <div class="title">{{count}}</div>

    <div class="todo-form">
      <input class="todo-input" type="text" placeholder="Enter your todo" />
      <div @click="add" class="todo-button">Add todo</div>
    </div>

    <div class="item completed">
      <div>
        <input type="checkbox" />
        <span class="name">Eat</span>
      </div>
      <div class="delete">Del</div>
    </div>
    <div class="item">
      <div>
        <input type="checkbox" />
        <span class="name">Eat</span>
      </div>
      <div class="delete">Del</div>
    </div>
    <div class="item">
      <div>
        <input type="checkbox" />
        <span class="name">Eat</span>
      </div>
      <div class="delete">Del</div>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    const count = ref(1123123);
    console.log(count.value);

    function add() {
      count.value++;
      console.log(count.value);
    }
    return { count, add };
  },
};



</script>

<style>
body {
  background: linear-gradient(to right, #0575e6, #83eaf1);
}
.completed {
  text-decoration: line-through;
}
.delete {
  color: red;
  cursor: pointer;
  user-select: none;
}
.item {
  display: flex;
  box-sizing: border-box;
  margin-top: 20px;
  margin-left: 1%;
  padding: 10px;
  width: 98%;
  border-radius: 20px;
  background-color: white;
  user-select: none;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  align-items: center;
  justify-content: space-between;
}
.todo-list {
  padding-top: 20px;
  width: 98%;
  height: 500px;
  background-color: white;
  border-radius: 20px;
  margin-top: 20px;
  margin-left: 1%;
}
.title {
  font-size: 30px;
  font-weight: bold;
  text-align: center;
  margin-top: 30px;
}
.todo-form {
  display: flex;
  margin-top: 20px;
  margin-left: 1%;
  margin-bottom: 30px;
}
.todo-input {
  padding-left: 20px;
  border: 1px solid #d9d9d9;
  border-radius: 20px 0 0 20px;
  outline: none;
  width: 60%;
  height: 30px;
}
.todo-button {
  padding-top: 2px;
  width: 20%;
  border-radius: 0 20px 20px 0;
  background: linear-gradient(to right, #0575e6, #83eaf1);
  color: white;
  text-align: center;
  line-height: 30px;
  cursor: pointer;
  user-select: none;
}
</style>
