<template>
  <div class="hello">
    <h1>Component 2: {{name}}</h1>
    <h1>Component 2: {{theme}}</h1>
  </div>
</template>

<script>
import store from "../store.js";
export default {
  mounted() {
    // setTimeout(() => {
    //   //store.commit('changeName', 'Twitch')
    //   store.set("name", "Jamie Pine");
    // }, 3000);
  },
  data: () => ({
    ...store.mapState()
  }),
  beforeCreate() {
    store.subscribe(this);
  }
};
</script>