<script setup>
import { useRouter, useRoute } from 'vue-router';
const route = useRoute();
const router = useRouter();
console.log(router.getRoutes());
</script>

<template>
    <div class="tabs is-centered">
        <ul>
            <li v-for="link in router.getRoutes()" :class="{ 'is-active': route.path === link.path }">
                <router-link :to="link.path">{{ link.name }}</router-link>
            </li>
        </ul>
    </div>
</template>