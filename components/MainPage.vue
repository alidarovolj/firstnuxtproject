<template>
  <div>
    <p @click="$router.push({ name: 'about' })">HomePage</p>
    <NuxtLink to="/singlePage">
      Главная
    </NuxtLink>
  </div>
</template>

<script>
export default {
  name: 'MainPage'
}
</script>
