<template>
  <nav class="nav">
    <div class="container">
      <div class="nav__box">
        <routerLink to="/" class="nav__logo">
          <h1 class="nav_logo_text">MY PORTFOLIO.</h1>
        </routerLink>
        <button class="nav__burger" @click="burger = true">
          <img src="../../assets/Images/menu.svg.png" alt="" />
        </button>
        <ul class="nav__list" :class="{ active: burger }">
          <button class="nav__close" @click="burger = false">
            <img src="../../assets/Images/close.jpg" alt="" />
          </button>
          <li>
            <routerLink to="/" class="nav__link">Home</routerLink>
          </li>
          <li>
            <routerLink to="/movie" class="nav__link">About</routerLink>
          </li>
          <li>
            <routerLink to="/tv" class="nav__link">Portfolio</routerLink>
          </li>
          <li>
            <routerLink to="/tv" class="nav__link">Contact</routerLink>
          </li>
   
        </ul>
      </div>
    </div>
  </nav>
</template>
<script setup>
import { ref } from "vue";
const burger = ref(false);
</script>
<style lang=""></style>
