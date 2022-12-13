<script setup lang="ts">
import { ref } from "vue";

const tab = ref("mails");
</script>

<template>
  <q-layout view="hHh lpR fFf">
    <q-header bordered class="bg-primary text-white" height-hint="98">
      <q-toolbar class="toolbar bg-primary rounded-borders" inset>
        <q-toolbar-title>
          <q-avatar square>
            <img
              src="https://thumbs.gfycat.com/ConventionalOblongFairybluebird-size_restricted.gif"
            />
          </q-avatar>
          <span class="text-accent text-weight-bold q-ml-md">Lojinha</span>
        </q-toolbar-title>
        <q-tabs v-model="tab" shrink inline-label>
          <q-route-tab
            id="button_home"
            class="bg-accent q-ma-xs"
            to="/"
            icon="home"
            label="Home"
          />
          <q-route-tab
            class="bg-accent q-ma-xs"
            to="/products"
            icon="shopping_cart"
            label="Carrinho"
          />
          <q-route-tab
            class="bg-accent q-ma-xs"
            to="/contact"
            icon="email"
            label="Contato"
          />
        </q-tabs>
      </q-toolbar>
      <q-tabs> </q-tabs>
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
