<template>
  <ul>
    <li><nuxt-link to="/">Strona główna</nuxt-link></li>
    <li>
      <nuxt-link to="/about">O nas</nuxt-link>
    </li>
    </ul>
<NuxtPage/>
</template>
<script setup>
const showModal = ref(false)

const emitModalShow = () => {
  showModal.value = !showModal.value
  console.log(showModal.value)
}
</script>