<template>
  <div>
    <h1>第一个页面</h1>
    <NuxtLink to="/list">进入列表页</NuxtLink>
  </div>
</template>

<script setup>
  const foo = useFoo();
  // *nuxt 常用 hook，不需要 import 就能用
  const appConfig = useAppConfig();
  console.log('111111111----', appConfig);

  const { data, pending, error, refresh } = await useAsyncData(
    'mountains',
    () => $fetch('https://api.nuxt.js.dev/mountains')
  )
</script>