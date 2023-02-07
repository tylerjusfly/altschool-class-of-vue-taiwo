<template>
    <h1>Color Picker Game</h1>

    <div>{{ message }}</div>

    <button v-for="color in colors" :key="color" @click="matchColor(color)">
        {{ color }}
    </button>
</template>

<script setup>
import { ref, reactive } from "@vue/reactivity";
import { UseColorPicker } from "../composables/UseColorPicker";

const { colors, message, matchColor } = UseColorPicker();
</script>

<style></style>
