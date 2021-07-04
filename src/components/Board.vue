<template>
  <div>
    <header>
      my Trello
    </header>
    <main>
      <p class="info-line">All: 0 tasks</p>
      <list-add />
    </main>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import ListAdd from'./ListAdd.vue'

export default defineComponent({
  components: { ListAdd },
  setup() {
  },
})
</script>
