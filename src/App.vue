<template>
  <base-container title="Vuex">
    <h3>{{ $store.state.counter }}</h3>
    <button @click="addOne">Add One</button>
    <TheAddDynamic />
  </base-container>
</template>

<script>
import BaseContainer from './components/BaseContainer.vue';
import TheAddDynamic from './components/TheAddDynamic.vue';


export default {
  components: {
    BaseContainer,
    TheAddDynamic
  },
  methods: {
    addOne(){
      this.$store.commit('increment')
    }
  }
};
</script>

<style>
* {
  box-sizing: border-box;
}

html {
  font-family: sans-serif;
}

body {
  margin: 0;
}
</style>