<script setup lang="ts">
import { useSlots, computed } from 'vue';

const slots = useSlots();
const hasSlotHeader = computed(() => Boolean(slots.header));
</script>

<template>
  <div class="card-access">
    <div class="card-access__wrapper">
      <div v-if="hasSlotHeader" class="card-access__header">
        <slot name="header" />
      </div>
      <div class="card-access__body">
        <slot />
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.card-access__wrapper {
  background-color: white;
  backdrop-filter: blur(3px);
  background-color: rgba(255, 255, 255, 0.2);
  border: 1px solid rgba(255, 255, 255, 0.2);
  // border: 1px solid rgb(0 0 0 / 8%);
  width: 100%;
  margin: auto;
  padding: 48px 52px;
  border-radius: 16px;
  color: white;
  box-shadow: 0px 5px 6px -6px rgb(0 0 0 / 20%);
}
.card-access__header {
  margin-bottom: 24px;
}
</style>
