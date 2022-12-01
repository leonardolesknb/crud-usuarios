<template>
  <div id="app">
    <main id="main">
      <BaseMenu />
      <transition mode="out-in">
        <router-view />
      </transition>
    </main>
  </div>
</template>

<script>
import BaseMenu from '@/components/BaseMenu.vue';

export default {
  name: "App",
  components:{
    BaseMenu
  }
};
</script>

<style>
@import url("./assets/css/main.css");
</style>