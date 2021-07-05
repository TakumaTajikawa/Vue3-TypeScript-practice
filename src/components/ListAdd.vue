<template>
  <form class="addlist" @submit.prevent="addList">
    <input v-model="title"
      type="text"
      class="text-input"
      placeholder="Add new list"
    >
    <button type="submit" class="add-button">
      Add
    </button>
  </form>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'

export default defineComponent({
  setup() {
    const title = ref('');

    const addList = () => {
      title.value = ''
    }

    return {
      addList,
    }
  },
  




})
</script>
