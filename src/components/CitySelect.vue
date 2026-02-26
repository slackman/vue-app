<script setup>
import { inject, ref } from 'vue';
import IconLocation from '../icons/IconLocation.vue';
import Button from './Button.vue';
import Input from './Input.vue';
import { cityProvide } from '../constants';

const city = inject(cityProvide);
const inputValue = ref(city.value);

let isEdited = ref(false);

function edit() {
    isEdited.value = true;
}

function select() {
    isEdited.value = false;
    city.value = inputValue.value;
}
</script>

<template>
    <div class="city-select">
        <div v-if="isEdited" class="city-input">
            <Input
                v-model="inputValue"
                v-model:additional="city"
                v-focus
                placeholder="Введите город"
                @keyup.enter="select()"
            />
            <Button @click="select()"> Сохранить </Button>
        </div>
        <Button v-if="!isEdited" @click="edit()">
            <IconLocation />
            Изменить город
        </Button>
    </div>
</template>

<style scoped>
.city-input {
    display: flex;
    gap: 12px;
}

.city-select {
    width: 420px;
}
</style>
