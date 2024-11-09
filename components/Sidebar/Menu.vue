<template lang="">
    <div>
     <header class='flex items-center gap-2 p-4 hover:scale-[100%] transition cursor-pointer'>
        <logo/>
        <p class='font-bold text-black'>Nuxt-Finance</p>
     </header>
     <div class='px-4 grow'>
        <div class='grid gap-4'>
            <NuxtLink :href="item.path" v-for="(item, index) in items" :key="index" class='flex items-center gap-2 px-2 py-1 transition rounded cursor-pointer hover:bg-neutral-100'>
                <Icon :name="item.icon || 'ic:baseline-help-outline'" color='black'/>
                <span >{{item.title}}</span>
            </NuxtLink>
        </div>
     </div>
    </div>
</template>

<script setup>
const items = ref([
    {
        title: 'Overview',
        path: "/",
        icon: 'ic:twotone-dashboard'
    },
    {
        title: 'Transactions',
        path: "/transactions",
        icon: 'uil:exchange'
    },
    {
        title: 'Account',
        path: "/",
        icon: 'mdi:account-circle-outline'
    },
    {
        title: 'Contacts',
        path: "/",
        icon: 'mynaui:telephone'
    },
    {
        title: 'Settings',
        path: "/",
        icon: 'ic:outline-settings'
    },
])
</script>