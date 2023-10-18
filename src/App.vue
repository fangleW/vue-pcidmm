<template>
  <div id="app"></div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import { ref, onMounted } from 'vue';
import { useMouse } from '@vueuse/core';
export default {
  name: 'App',
  components: {
    HelloWorld,
  },
};
console.log(99, useMouse());
onMounted(() => {
  const { x, y } = useMouse();
  console.log(222, x.value, y);
});
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
