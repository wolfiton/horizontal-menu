<template>
  <div id="q-app">
    <router-view />
  </div>
</template>

<script>
export default {
  name: "App"
};
</script>

<style>
.hmenu-enter-active,
.hmenu-leave-active {
  opacity: 1;
  margin-left: 10px;
  transition: all 1s ease-out;
}
.hmenu-enter,
.hmenu-leave-to {
  opacity: 0;
  margin-left: -300px;
  transition: all 1s ease-in-out;
}
</style>
