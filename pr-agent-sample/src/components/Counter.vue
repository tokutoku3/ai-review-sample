<template>
    <div class="card">
      <button type="button" @click="count++">count is {{ count }}</button>
      <p :class="countText">{{ countText }}</p>
    </div>
  </template>
  
  <script setup lang="ts">
  import { ref, computed } from 'vue'
  
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