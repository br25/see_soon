<template>
  <div class="home">
    <Sidebar />
    <Dashboard />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

import Sidebar from "@/components/Sidebar.vue"; // @ is an alias to /src
import Dashboard from "@/components/Dashboard.vue";

export default defineComponent({
  name: "HomeView",
  components: {
    Sidebar,
    Dashboard,
  },
});
</script>
