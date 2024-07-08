<script setup lang="ts">
import { ref } from 'vue'
import { CountTo } from '@vben/components'
import { add } from '@vben/math/add'

defineProps<{ msg: string }>()

const count = ref(0)
</script>

<template>
  <h1>{{ msg }}</h1>

  <div class="card">
    <button type="button" @click="count++">count is {{ count }}</button>
    <p>
      Edit
      <code>components/HelloWorld.vue</code> to test HMR
    </p>

    <CountTo />
    <div>
      {{ add(1, 4) }}
    </div>
  </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
