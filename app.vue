<script setup>
  const menu = [
    {
      title: 'Home',
      path: '/'
    },
    {
      title: 'About',
      path: '/about_page'
    },
    {
      title: 'Contact',
      path: '/contact_page'
    },
    {
      title: 'Shop',
      path: '/shop'
    }
  ];
</script>

<template>
  <h2>Layout and Pages</h2>
  <ul v-if="menu">
    <li v-for="(item, index) in menu" :key="index">
      <NuxtLink :to="item.path">{{ item.title }}</NuxtLink>
    </li>
  </ul>
  <NuxtPage />
</template>
