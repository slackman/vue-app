<script setup>

</script>

<template>
    <button class="button_game">
        <slot></slot>
    </button>
</template>

<style scoped>
.button_game {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
    padding: 16px 10px;
    width: 315px;
    min-height: 68px;
    border: 0;
    border-radius: 100px;
    background: var(--color-bg-btn-game);
    color: #fff;
    font-family: Roboto, sans-serif;
    font-size: 24px;
    line-height: 36px;
    font-weight: 400;
}

.button_game:hover { background: var(--color-bg-btn-game-hover); }
</style>