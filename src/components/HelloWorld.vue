<script setup>
import { ref } from 'vue'

defineProps({
  msg: String
})

const count = ref(0)
const isVisible = ref(true)
function toggleMsg() {
	isVisible.value = !isVisible.value;
}
</script>

<template>
  <h1 v-if="isVisible">{{ msg }}</h1>

  <p>
    Welcome:
    <a href="https://hx.dcloud.net.cn/" target="_blank">HBuilderX</a>
  </p>

  <p>
    <a href="https://vitejs.dev/guide/features.html" target="_blank">
      Vite Documentation
    </a>
    |
    <a href="https://v3.vuejs.org/" target="_blank">Vue 3 Documentation</a>
  </p>
  <button type="button" @click="toggleMsg">Toggle Message</button>
  <button type="button" @click="count++">count is: {{ count }}</button>
  <p>
  </p>
</template>

<style scoped>
a {
  color: #42b983;
}
</style>
