<template>
  <div id="appp">
    <div class="head">
      <div>submitted date</div>
      <div>submitted date</div>
      <div>submitted date</div>
      <div>submitted date</div>
      <div>submitted date</div>
      <div>submitted date</div>
      <div>submitted date</div>
    </div>
    <div id="app">
      <SubComp id="subcomp" v-for="item in 5" v-bind:key="item"> </SubComp>
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
};
</script>

<style lang="scss">
.head {
  display: flex;
  margin-top: 10px;
}
#subcomp {
  overflow: auto;
  border: 1px solid black;
  width: 110%;
  height: 150px;
  background: #eee;
}
#app {
  border: 5px solid black;
  width: 100%;
  height: 405px;
  overflow: auto;
}
</style>
