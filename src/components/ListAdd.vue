<template>
  <form class="addlist" @submit.prevent="addList">
    <input v-model="title"
      type="text"
      class="text-input"
      placeholder="Add new list"
      @focusin="startEditing"
      @focusout="finishEditing"
    >
    <button type="submit" class="add-button">
      Add
    </button>
  </form>
</template>

<script lang="ts">
import { defineComponent, ref, computed } from 'vue'

export default defineComponent({
  setup() {
    const title = ref('');
    const isEditing = ref(false);

    const addList = () => {
      title.value = ''
    }

    const startEditing = ():void => {
      isEditing.value = true
    }

    const finishEditing = ():void => {
      isEditing.value = false
    }

    const classList = computed(() => {
      let classList = ref('addlist');
      if (isEditing.value) {
        classList.value.push('active');
      }
      return classList;
    })



    return {
      addList,
      startEditing,
      finishEditing,
      classList,
    }
  },
  




})
</script>
