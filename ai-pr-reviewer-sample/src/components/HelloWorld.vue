<template>
  <div>
    <h1>{{ msg }}</h1>

    <div class="card">
      <Counter />
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
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import Counter from './Counter.vue'

defineProps<{ msg: string }>()

const count = ref(0)
</script>

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
