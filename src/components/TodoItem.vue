<template>
  <div  class="todo_item" @click="removeTodo" @dblclick="changeTodo">
       <h1>{{ title }}</h1>
</div>
  
</template>

<script>
export default {
  props: ['title', 'completed', 'id'],
  emits: ['changeTodo', 'removeTodo'],
  methods: {
    changeTodo() {
      this.$emit('changeTodo', this.id)
    },
    removeTodo() {
      this.$emit('removeTodo', this.id)
    }
  }
}
</script>

<style scoped></style>
