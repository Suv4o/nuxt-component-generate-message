<template>
    <div>
        <h1>{{ word }}</h1>
        <button @click="generateRandomWord">Generate a Word</button>
    </div>
</template>

<script setup>
import { ref } from "vue";
import randomWords from "random-words";

const word = ref("");

function generateRandomWord() {
    word.value = randomWords();
}
</script>
