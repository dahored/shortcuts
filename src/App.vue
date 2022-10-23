<script setup lang="ts">
import { RouterView } from 'vue-router';
</script>

<template>
  <div class="app-template">
    <img
      class="app-template__background"
      alt="background"
      src="@/assets/backgrounds/img_background_1.jpg"
    />
    <div class="app-template__backdrop"></div>
    <div class="app-template__wrapper">
      <RouterView class="app-template__router-view" />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.app-template {
  position: relative;
  height: 100%;
}

.app-template__background,
.app-template__backdrop {
  position: fixed;
  width: 100%;
  height: 100%;
  z-index: 2;
}

.app-template__background {
  object-fit: cover;
  object-position: center center;
}

.app-template__backdrop {
  // background-color: rgba(255, 255, 255, 0.4);
  background-color: rgba(0, 0, 0, 0.3);
}

.app-template__wrapper {
  position: relative;
  z-index: 3;
  min-height: 100%;
  // background: rgb(255, 255, 255);
  // background: linear-gradient(
  //   0deg,
  //   rgba(255, 255, 255, 0.8995973389355743) 0%,
  //   rgba(255, 255, 255, 0.5746673669467788) 40%,
  //   rgba(255, 255, 255, 0) 100%
  // );
  background: rgb(0, 0, 0);
  background: linear-gradient(
    0deg,
    rgba(0, 0, 0, 0.8995973389355743) 0%,
    rgba(0, 0, 0, 0.5746673669467788) 40%,
    rgba(0, 0, 0, 0) 100%
  );
}

.app-template__router-view {
  max-width: 1200px;
  // background-color: red;
  margin: auto;
  padding: 120px 24px 40px;
}
</style>
