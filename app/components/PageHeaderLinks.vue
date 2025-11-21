<script setup lang="ts">
import { useClipboard } from '@vueuse/core'

const { copied } = useClipboard()
const isCopying = ref(false)
</script>

<template>
  <UButtonGroup>
    <UButton
      label="Copy page"
      :icon="copied ? 'i-lucide-copy-check' : 'i-lucide-copy'"
      color="neutral"
      variant="outline"
      :loading="isCopying"
      :ui="{
        leadingIcon: [copied ? 'text-primary' : 'text-neutral', 'size-3.5']
      }"
    />
  </UButtonGroup>
</template>
