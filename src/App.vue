<script setup>
import Button from './components/Button.vue';
import ButtonPlay from './components/ButtonPlay.vue';
</script>

<template>
  <main class="main">
    <Button>Сохранить</Button>
  </main>
  <div>
    <ButtonPlay>Начать игру</ButtonPlay>
  </div>
</template>

<style scoped>
.main {
  background: var(--color-bg-main);
  padding: 60px 50px;    
  border-radius: 25px;
}
</style>
