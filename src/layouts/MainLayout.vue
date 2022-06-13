<script setup lang="ts">
import { ref } from 'vue';

const tab = ref('mails');

</script>

<template>
  <q-layout view="hHh lpR fFf">
    <q-header
      bordered
      class="bg-primary text-white"
      height-hint="98"
    >
      <q-toolbar
        class="toolbar glossy bg-accent rounded-borders"
        inset
      >
        <q-toolbar-title>
          <q-avatar square>
            <img src="../assets/images/logo.jpg">
          </q-avatar>
          <span class="text-primary text-weight-bold q-ml-md">Denisinha Store</span>
        </q-toolbar-title>
        <q-tabs
          v-model="tab"
          shrink
          inline-label
        >
          <q-route-tab
            class="bg-secondary q-ma-xs"
            to="/"
            icon="home"
            label="Home"
          />
          <q-route-tab
            class="bg-secondary q-ma-xs"
            to="/products"
            icon="shopping_cart"
            label="Loja"
          />
          <q-route-tab
            class="bg-secondary q-ma-xs"
            to="/contact"
            icon="email"
            label="Contato"
          />
        </q-tabs>
      </q-toolbar>
      <q-tabs>
      </q-tabs>
    </q-header>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<style lang="scss" scoped>
.toolbar {
  border-bottom: $accent 5px double;
  box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.1);
}
</style>
