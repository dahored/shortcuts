<script setup lang="ts">
import Card from '@/components/atoms/Card.vue';
</script>

<template>
  <div class="login-module">
    <div class="login-module__wrapper">
      <Card>
        <template v-slot:header>
          <h2>Login</h2>
        </template>
        <div class="login-module__form"></div>
      </Card>
    </div>
  </div>
</template>

<style lang="scss">
.login-module__wrapper {
  max-width: 420px;
  margin: auto;
}
</style>
