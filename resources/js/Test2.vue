<template>
    <div>
        <p>Test component 2</p>
        <p>{{ message }}</p>
    </div>
</template>
<script setup>
import { ref } from 'vue';

const message = ref('');
</script>
