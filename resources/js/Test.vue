<template>
    <div>
        <p>Test component 1</p>
        <p>{{ message }}</p>
    </div>
</template>
<script setup>
import { ref } from 'vue';

const message = ref('');
</script>
