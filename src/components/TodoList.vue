<script >
import TodoItem from './TodoItem.vue'
export default {
    data() {
        return {
            todos: [
                {
                    "id": 1,
                    "text": "Item 1",
                },
                {
                    "id": 2,
                    "text": "Item 2",
                }
            ],

            idInc: 0

        }
    },


    components: {
        TodoItem,
    },


    methods: {
        addItem: function (event) {
            console.log(event.target.value)
            idInc = this.todos.length++
             this.todos[idInc].id
            
            text = this.todos.text
        }
    }
}
</script>

<template lang="">
    <h1>Todo </h1>
<ul>
    <TodoItem  v-for="todo in todos" :key="todo.id" :todo="todo" />
</ul>

<input type="text" id="addinput" v-model="text" >

  <button @click="addItem">


  </button>

    
</template>

<style lang="">
    
</style>