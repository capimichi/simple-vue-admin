<template>
  <div class="flex h-screen overflow-hidden">
    <Sidebar/>
    <div class="relative flex flex-1 flex-col overflow-y-auto overflow-x-hidden">
      <Header/>
      <main>
        <slot/>
      </main>
    </div>
  </div>
</template>
<script setup lang="ts">
import Sidebar from "~/components/Dashboard/Sidebar.vue";
import Header from "~/components/Dashboard/Header.vue";
</script>