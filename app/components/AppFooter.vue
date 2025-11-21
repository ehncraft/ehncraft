<script setup lang="ts">
const { footer } = useAppConfig()
</script>

<template>
  <UFooter>
    <template #left>
      <!-- {{ footer.credits }} -->
    </template>

    <template #right>
      <UColorModeButton v-if="footer?.colorMode" />
    </template>
  </UFooter>
</template>
