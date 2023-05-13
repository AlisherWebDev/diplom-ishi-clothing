<template>
  <footer class="footer">
    <BaseDivider />
    <router-link
      to="/"
      :class="[
        'header__logo',
        isHomepage ? 'header__logo-disabled' : 'header__logo_active',
      ]"
      disabled="true"
    >
      <img src="@/assets/logo.svg" class="footer__logo" />
    </router-link>
  </footer>
</template>

<script setup>
import BaseHeading from "./UI/BaseHeading.vue";
import BaseDivider from "@/components/UI/BaseDivider.vue";
</script>

<style scoped>
.footer {
  display: flex;
  justify-content: center;
  align-items: center;
  color: lightgray;
  justify-self: center;
  align-self: center;
  height: 100%;
}
.footer__logo {
  width: 110px;
  color: lightgray;
  text-decoration: none;
}
.footer__logo-disabled {
  pointer-events: none;
}

.footer__logo_active {
  color: #ffa801;
}

.footer__logo_active:hover {
  opacity: 0.6;
  transition: opacity 0.3s ease-in;
}

@media screen and (min-width: 768px) {
  .footer__logo {
    width: 160px;
  }
}
</style>
