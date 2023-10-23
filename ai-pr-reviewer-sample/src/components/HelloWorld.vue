<script setup lang="ts">
import { ref, computed } from 'vue'

defineProps<{ msg: string }>()

const count = ref(0)

const countText = computed(() => {
  const remainder = count.value % 3
  if (remainder === 0) {
    return 'hoge'
  } else if (remainder === 1) {
    return 'fuga'
  } else {
    return 'piyo'
  }
})
</script>

<template>
  <h1>{{ msg }}</h1>

  <div class="card">
    <button type="button" @click="count++">count is {{ count }}</button>
    <p :class="countText">{{ countText }}</p>
    <p>
      Edit
      <code>components/HelloWorld.vue</code> to test HMR
    </p>
  </div>

  <p>
    Check out
    <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank"
      >create-vue</a
    >, the official Vue + Vite starter
  </p>
  <p>
    Install
    <a href="https://github.com/vuejs/language-tools" target="_blank">Volar</a>
    in your IDE for a better DX
  </p>
  <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}

.hoge {
  color: red;
  font-size: 24px;
}

.fuga {
  color: blue;
  font-size: 18px;
}

.piyo {
  color: green;
  font-size: 12px;
}
</style>
