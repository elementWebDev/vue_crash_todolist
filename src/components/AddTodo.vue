<template>
	<div>
		<form @submit="addTodo">
			<input type="text" v-model="title" name="title" placeholder="Add Todo...">
			<input type="submit" value="Submit" class="btn">
		</form>
	</div>
</template>

<script>
// import uuid from 'uuid';
export default {
	name: "AddTodo",
	data() {
		return {
			todos: []
			//title: ''
			// to add more info (such as name etc., you would add here)
		}
	},
	methods: {
		addTodo(e) {
			e.preventDefault();
			const newTodo = {
				//id: uuid.v4(),
				title: this.title,
				completed: false // always false when todo is created
			}
			// Send up to parent
			this.$emit('add-todo', newTodo);

			this.title = '';
		}
	}
}
</script>

<style scoped>
	form {
		display: flex;
	}

	input[type="text"] {
		flex: 10;
		padding: 5px;
	}

	input[type="submit"] {
		flex: 2;
	}
</style>
