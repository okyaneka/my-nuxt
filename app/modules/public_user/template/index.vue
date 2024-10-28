<script setup lang="ts">
import { NButton } from "naive-ui";
import { useTitle } from "@vueuse/core";

const isDark = useDark();
const toggleDark = useToggle(isDark);

useTitle("p");
</script>

<template>
  <div>
    <h1 class="text-3xl text-primary">Welcome to the homepage</h1>
    <NButton type="primary" @click="toggleDark()"> Button </NButton>
  </div>
</template>
