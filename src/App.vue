<template>
  <div id="app">
    <main id="container">
      <SubComp id="subcomp" v-for="item in 5" v-bind:key="item"></SubComp>
    </main>
    <div id="scrollContainer" v-on:scroll="handleScroll">
      <div id="fakeDiv"></div>
    </div>
  </div>
</template>

<script>
import SubComp from "./components/SubComp.vue";

export default {
  name: "App",
  components: {
    SubComp,
  },
  methods:{
    handleScroll(e) {
      let els = document.getElementsByClassName('paraClass')
      for (let index = 0; index < els.length; index++) {
        const element = els[index];
        element.scrollLeft = e.target.scrollLeft;
      }
    }
  }
};
</script>

<style lang="scss">
#container {
  border: 5px solid black;
  width: auto;
  height: 90vh;
  overflow-y: auto;
  overflow-x: hidden;
}
#scrollContainer{
  height: 20px;
  width: 100vw;
  overflow-x: scroll;
}
#fakeDiv{
  width: 200vw;
}
</style>
