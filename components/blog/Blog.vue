<template>
    <div class="border m-3 p-5">
        <p>{{blog.title}}</p>
        <p>{{blog.description}}</p>
    </div>
    
</template>
<script setup>
const props = defineProps({
    blog: Object
})
</script>
