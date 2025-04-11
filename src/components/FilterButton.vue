<script lang="ts" setup>
import type { TaskFilter } from "../types";

const props = defineProps<{
  filter: TaskFilter;
}>();

const emits = defineEmits<{
  setFilter: [filter: TaskFilter];
}>();
</script>

<template>
  <button class="secondary" @click="emits('setFilter', props.filter)">
    {{ props.filter }}
  </button>
</template>

<style scoped>
button {
  text-transform: capitalize;
}
</style>
