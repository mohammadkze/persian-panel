<template>
  <component :is="layout">
    <router-view />
  </component>
</template>
<script lang="ts" setup>
import { computed } from 'vue'
import { useRouter } from 'vue-router'

const defaultLayout = 'default'

const { currentRoute } = useRouter()

const layout = computed(
  () => `${currentRoute.value.meta.layout || defaultLayout}-layout`
)
</script>

<style>
  @font-face {
  font-family: "Qs_Iranyekan light";
    src: local("Qs_Iranyekan light"), 
    url('./assets/fonts/Qs_Iranyekan light.ttf') format('truetype');
  font-weight: normal;
  font-style: normal;
  };
  * {
    font-family: "Qs_Iranyekan light"
  };
</style>
