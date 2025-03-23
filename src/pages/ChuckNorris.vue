<template>
    <div class="container">
        <div class="content">
            <h2>{{ joke }}</h2>
        </div>
    </div>
</template>
<script setup>
import axios from 'axios';
import { ref } from 'vue';
let joke = ref('');
let response = await axios.get('https://api.chucknorris.io/jokes/random');
joke.value = response.data.value;
</script>