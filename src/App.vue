<script setup lang="ts">
useHead({
  meta: [
    { property: 'og:title', content: 'MerlinAlex' },
    // TODO: content
    { property: 'og:image', content: 'https://antfu.me/avatar.png' },
    { name: 'description', content: 'MerlinAlex\'s Portfolio' },
    { name: 'twitter:card', content: 'summary' },
    { name: 'twitter:creator', content: '@Jingping_Huang' },
  ],
})
</script>

<template>
  <NavBar />
  <main class="px-7 py-10">
    <router-view />
    <Footer />
  </main>
</template>
