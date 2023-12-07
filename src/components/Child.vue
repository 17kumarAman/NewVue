<script setup>
defineProps(['data'])
defineEmits(['events'])


</script>

<template>

    <div>
        <h4 v-for="e in data">
            {{ e }}
            <button @click="$emit('events', e)">Emits</button>
        
        </h4>
    </div>
</template>
