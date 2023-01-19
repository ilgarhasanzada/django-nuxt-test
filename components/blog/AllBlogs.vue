<template>
    <div class="grid grid-cols-2">
        <Blog :key="blog" v-for="blog in blogs" :blog="blog"/>
    </div>
    <input v-model="form_data.title" type="text" class="border-2 border-black m-5">
    <input v-model="form_data.description" type="text" class="border-2 border-black m-5">
    <button @click="add_data()" class="border-2 p-2">ADD</button>
    {{show_data}}
</template>
<script setup>
    const {data: blogs} = await useAsyncData('blogs',()=>
        $fetch('http://localhost:8000/blogs/')    
    )
    const form_data = ref({
        "title":"",
        "description":""
    })
    let show_data = ref()
    
    async function add_data(){
        await $fetch( 'http://localhost:8000/blogs/', {
        method: 'POST',
        body: this.form_data
    } );
    this.show_data=this.form_data.data;
        this.form_data.data="";
    }
</script>