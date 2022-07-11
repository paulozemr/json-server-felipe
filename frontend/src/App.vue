<script setup>
import HeaderComp from "@/components/template/HeaderComp.vue";
import FooterComp from "@/components/template/FooterComp.vue";
</script>

<template>
  <HeaderComp />
  <main>
    <RouterView />
  </main>
  <FooterComp />
</template>

<style>
@import "@/assets/base.css";
@import "@/assets/style.css";

#app {
  margin: 0 auto;
  font-weight: normal;
  height: 100vh;
}

header,
footer {
background-image: linear-gradient(45deg, #8fe0e0 25%, #F6F0CF 25%, #F6F0CF 50%, #8fe0e0 50%, #8fe0e0 75%, #F6F0CF 75%, #F6F0CF 100%);
  background-size: 56.57px 56.57px;
  color: rgb(0, 0, 0);
  height: 15%;
  font-size: 1.3rem;
  display: flex;
  align-items: center;
  padding-left: 2rem;
}

main {
  height: 70%;
}
</style>
