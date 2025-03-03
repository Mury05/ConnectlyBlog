<script lang="ts" setup>
const links = [
    {
        label: 'Blog',
        to: '/blog',
    },
    {
        label: 'A propos',
        to: '/about',
    }
];

</script>


<template>

    <UHeader>
        <template #left>
            <NuxtLink to="/">
                <img src="/logo.png" alt="Logo de Connectly" class="w-auto h-6 shrink-0">
            </NuxtLink>
        </template>

        <template #center>
            <UHeaderLinks :links="links" class="hidden lg:flex" />
        </template>

        <template #right>
            <div class="hidden lg:flex">

                <UButton label="Se connecter" variant="link" color="orange" to="/login" />
            </div>
            <UColorModeButton />
        </template>

        <template #panel>
                <UHeaderPopoverLinks :links="links" />
                <UButton label="Se connecter" variant="link" color="orange" to="/login" />
                <UColorModeButton />

        </template>
    </UHeader>

</template>


<style scoped></style>