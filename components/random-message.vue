<template>
    <div>
        <h1>{{ msg }}</h1>
        <button @click="changeMsg">Generate a Message</button>
    </div>
</template>

<script setup>
import { ref } from "vue";
const msg = ref("");
const changeMsg = () => {
    msg.value = makeid(getRandomInt(100));
};

function makeid(length) {
    var result = "";
    var characters = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789";
    var charactersLength = characters.length;
    for (var i = 0; i < length; i++) {
        result += characters.charAt(Math.floor(Math.random() * charactersLength));
    }
    return result;
}

function getRandomInt(max) {
    return Math.floor(Math.random() * max);
}
</script>
