<template>
  <ul id="myUL">
            <template v-for="(todo) in todos" :key="todo.no">
                <li :class="{checked : todo.todoyn ==1}" @click="todoUpdate(todo)">
                    {{todo.contents}}
                    <span class="close" @click.stop="todoDelete(todo.no)">X</span>
                </li>
            </template>
        </ul>
</template>

<script>
export default {
    name: "TodoList",
    methods: {
        todoDelete(todo.no){
            this.$emit('s')
        }
    }
}
</script>

<style>

</style>