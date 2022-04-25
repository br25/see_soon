<template>
  <nav>
    <n-space justify="space-between">
      <n-icon size="40">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          viewBox="0 0 512 512"
        >
          <path
            fill="none"
            stroke="currentColor"
            stroke-linecap="round"
            stroke-miterlimit="10"
            stroke-width="48"
            d="M88 152h336"
          ></path>
          <path
            fill="none"
            stroke="currentColor"
            stroke-linecap="round"
            stroke-miterlimit="10"
            stroke-width="48"
            d="M88 256h336"
          ></path>
          <path
            fill="none"
            stroke="currentColor"
            stroke-linecap="round"
            stroke-miterlimit="10"
            stroke-width="48"
            d="M88 360h336"
          ></path>
        </svg>
      </n-icon>
      <div class="route">
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link>
      </div>
      <n-avatar
        :style="{
          color: 'yellow',
          backgroundColor: 'red',
        }"
      >
        M
      </n-avatar>
    </n-space>
  </nav>
  <router-view />
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Header",
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
nav {
  padding: 10px;
  background: #eeeeee;
}

.route {
  margin: 10px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
