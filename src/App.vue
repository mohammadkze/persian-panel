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
  font-family: "FontFree-Net-ir_sans";
    src: local("FontFree-Net-ir_sans"), 
    url('./assets/fonts/FontsFree-Net-ir_sans.ttf') format('truetype');
  font-weight: normal;
  font-style: normal;
  };
  * {
    font-family: "FontFree-Net-ir_sans"
  };
</style>
