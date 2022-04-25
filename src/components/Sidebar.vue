<template>
  <div class="sidebar" :open="sidebarOpened" @close="sidebarOpened = false">
    <n-button @click="sidebarOpened = false">
      <n-icon size="40" :class="{ 'rotate-180': collapsed }"
         class="collapse-icon">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          viewBox="0 0 24 24"
        >
          <g
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          >
            <circle cx="12" cy="12" r="9"></circle>
            <path d="M10 10l4 4m0-4l-4 4"></path>
          </g>
        </svg>
      </n-icon>
    </n-button>
    <div>
      <div class="route">
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link>
      </div>
      <router-view />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref, computed } from "vue";

export default defineComponent({
  name: "Sidebar",


  data() {
    return {
      sidebarOpened: true,
    }
  }
});




</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.sidebar {
  background: #fbf8f1;
  item-hover: #454541;
  item-active: #451157;
  width: 30%;
  height: 100vh;
  color: black;
  float: left;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 0;
  bottom: 0;
  padding: 0.5em;
  transition: 0.3s ease;
  display: flex;
  flex-direction: column;
  
}

.collapse-icon {
  position: absolute;
  top: 0;
  right: 0;
  padding: 0.75em;
  color: black;
  transition: 0.2s linear;
}
.rotate-180 {
  transform: rotate(180deg);
  transition: 0.2s linear;
}

.route {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.route a {
  font-weight: bold;
  color: #2c3e50;
}

.route a.router-link-exact-active {
  color: #42b983;
}



@media only screen and (max-width: 600px) {
  .sidebar {
    width: 100%;
    visibility: visible;
  }
}
</style>
