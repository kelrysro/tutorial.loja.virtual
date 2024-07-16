<script setup></script>
<template>
   <div id="footerMenu" :style="{ display: showMenu ? 'block' : 'none' }">
    <RouterLink to="/">
      <i class="mdi mdi-home-outline" />
      Home
    </RouterLink>
    <RouterLink to="/login">
      <i class="mdi mdi-account" />
      Login
    </RouterLink>
  </div>
  <div class="icons">
    <RouterLink to="/">
      <i class="mdi mdi-home-outline" />
      Home
    </RouterLink>
    <RouterLink to="/">
      <i class="mdi mdi-account-circle-outline" />
      Perfil
    </RouterLink>
    <RouterLink to="/">
      <i class="mdi mdi-cart-outline" />
      Carrinho
    </RouterLink>

    <div class="hamburger" @click="showMenu = !showMenu">
      <i class="mdi mdi-menu" />
      Menu
    </div>
  </div>
</template>
<style setup>
import { ref } from 'vue';
import { onBeforeRouteUpdate } from 'vue-router';

const showMenu = ref(false);

onBeforeRouteUpdate(() => {
  showMenu.value = false;
});
</style>
