<template>
  <div id="app">
		<AddTodo v-on:add-todo="addTodo" />
    <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo" />
  </div>
</template>

<script>

import Todos from '../components/Todos';
import AddTodo from '../components/AddTodo';
import axios from 'axios';

export default {
  name: 'Home',
  components: {
		Todos,
		AddTodo
	},
	data() {
		return {
			todos: [
				{
					id: 1,
					title: "Todo One",
					completed: false
				},
				{
					id: 2,
					title: "Todo Two",
					completed: false
				},
				{
					id: 3,
					title: "Todo Three",
					completed: false
				}
			]
		}
	},
	methods: {
		deleteTodo(id) {
			axios.delete(`https://jsonplaceholder.typicode.com/todos/${id}`)
				.then(res => this.todos = this.todos.filter(todo => todo.id !== id))
				.catch(err => console.log(err));
		},
		addTodo(newTodo) { // LEFT OFF: https://youtu.be/Wy9q22isx3U?t=3583
			const { title, completed } = newTodo;

			axios.post('https://jsonplaceholder.typicode.com/todos', {
				title,
				completed
			})
				.then(res => this.todos = [...this.todos, res.data])
				.catch(err => console.log(err));
		}
	},
	created() {
		axios.get('https://jsonplaceholder.typicode.com/todos?_limit=5') // need to build api
			.then(res => this.todos = res.data)
			.catch(err => console.log(err))
	}
}
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

	.btn {
		display: inline-block;
		border: none;
		background: #555;
		color: #fff;
		padding: 7px 20px;
		cursor: pointer;
	}

	.btn:hover {
		background: #666;
	}
</style>
