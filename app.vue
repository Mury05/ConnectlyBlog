<script setup lang="ts">
const colorMode = useColorMode()
const color = computed(() => colorMode.value === 'dark' ? '#111827' : 'white' )
useHead({
  title: "Connectly",
  htmlAttrs: {
    lang: 'fr'
  },
  link: [
    {rel: 'icon', href: '/favicon.ico'}
  ],
  meta: [
    {charset: 'utf-8'},
    {name: 'viewport', content: 'width=device, initial-scale=1.0'},
    {name:'theme-color', content: color}
  ]
})
</script>
<template>
  <div>
    <NuxtLayout >
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>
