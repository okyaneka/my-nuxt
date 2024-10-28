<script setup lang="ts">
import {
  darkTheme,
  NConfigProvider,
  NLayout,
  type GlobalThemeOverrides,
} from "naive-ui";

const isDark = useDark();

const theme: GlobalThemeOverrides = {};
</script>

<template>
  <NConfigProvider :theme="isDark ? darkTheme : null" :theme-overrides="theme">
    <NLayout class="min-h-screen">
      <div>isDark: {{ isDark }}</div>
      <NuxtPage />
    </NLayout>
  </NConfigProvider>
</template>
