<template>
  <div class="app">
    <p>{{ name }} - {{ code }}</p>
    <button @click="changeName('Eko')">Change Name</button>
    <button @click="changeCode('2')">Change Code</button>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'App',
  components: {
  },
  setup() {
    const name = ref('Lagos');
    const code = ref<number | string>(1);

    return { name, code }
  },
  methods: {
    changeName(name: string) {
      this.name = name;
      return name;
    },
    changeCode(code: number | string) {
      this.code = code;
      return code;
    }
  }
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