<script setup>
import { storeToRefs } from 'pinia';

import { useAuthStore } from '@/stores';

const authStore = useAuthStore();
const { user } = storeToRefs(authStore);
</script>

<template>
    <div v-if="user">
        <h1>Hi {{user.firstName}}!</h1>
        <label>Your Name</label>
        <p>{{user.firstName}} {{user.lastName}}</p>
        <label>Your User Id</label>
        <p>{{user.username}}</p>
    </div>
</template>
