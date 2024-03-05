<script setup>
const props = defineProps(["title", "id", "body", "colorText"])
console.log(props.title);
console.log(props.id);
</script>

<template>
    <div class="card">
        <div class="card-body">
            <h5 class="card-title" :class="`text-${colorText}`">{{ id }} - {{ title }}</h5>
            <p>{{ body }}</p>
        </div>
    </div>
</template>