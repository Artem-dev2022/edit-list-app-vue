<script>
import MainPage from './components/MainPage.vue';
export default {
  components: {MainPage},
  data() {
    return {
      array: [
        {
          "name": "foo1",
          "value": "bar1",
        },
        {
          "name": "foo2",
          "value": "bar2",
        },
        {
          "name": "foo3",
          "value": "bar3",
        },
        {
          "name": "foo4",
          "value": "bar4",
        },
        {
          "name": "foo5",
          "value": "bar5",
        },
        {
          "name": "foo6",
          "value": "bar6",
        },
        {
          "name": "foo7",
          "value": "bar7",
        },
        {
          "name": "foo8",
          "value": "bar8",
        },
        {
          "name": "foo9",
          "value": "bar9",
        },
        {
          "name": "foo10",
          "value": "bar10",
        },
        {
          "name": "foo11",
          "value": "bar11",
        },
        {
          "name": "foo12",
          "value": "bar12",
        },
        {
          "name": "foo13",
          "value": "bar13",
        },
        {
          "name": "foo14",
          "value": "bar14",
        },
        {
          "name": "foo15",
          "value": "bar15",
        },
        {
          "name": "foo16",
          "value": "bar16",
        },
        {
          "name": "foo17",
          "value": "bar17",
        },
        {
          "name": "foo18",
          "value": "bar18",
        },
        {
          "name": "foo19",
          "value": "bar19",
        },
        {
          "name": "foo20",
          "value": "bar20",
        }
      ]
    }
  }
}
</script>

<template>
  <header>
      <img src="./assets/vite.svg" class="logo" alt="Vite logo" />
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
  </header>

  <MainPage :array="array"/>
</template>

<style scoped>
header {
  padding: 10px 0;
  display: flex;
  gap: 20px;
  width: 100%;
}
.logo {
  height: 6em;
  will-change: filter;
  transition: filter 300ms;
  width: 50px;
  height: 50px;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
