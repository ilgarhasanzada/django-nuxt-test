<template>
    <nav class="bg-blue-900 px-10 text-white py-5 text-xl flex items-center justify-between">
        <ul class="flex text-4xl text-lime-400">
            <li><NuxtLink>DARCIN</NuxtLink></li>
        </ul>
        <ul class="flex text-amber-500 cursor-pointer">
            <li class="ml-5 hover:text-amber-300"><NuxtLink to="/">Home</NuxtLink></li>
            <li class="ml-5 hover:text-amber-300"><NuxtLink to="/sda">About</NuxtLink></li>
            <li class="ml-5 hover:text-amber-300"><NuxtLink to="/blog">Blog</NuxtLink></li>
            <li class="ml-5 hover:text-amber-300"><NuxtLink>Contact</NuxtLink></li>
        </ul>
    </nav>
    <slot/>

</template>