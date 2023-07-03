<template>
  <div id="subcomp" class="paraClass" ref="paraRef">
    <p id="para">
      provident dolor beatae aut ut mollitia ullam.re nostrum aliquam voluptatum
      dolorem provident dolor beatae aut ut mollitia ullam. Lorem ipsum dolor sit
      amet consectetur adipisicing elit. Vero deleniti veritatis labore molestiae
      architecto aspernatur esse ipsam placeat velit natus quisquam error, dicta
      doloremque exercitationem optio? Minus numquam accusamus veritatis unde
      aspernatur accusantium qui, voluptate officiis possimus dolore inventore
      nostrum aliquam voluptatum dolorem provident dolor beatae aut ut mollitia
      ullam. possimus dolore inventore nostrum aliquam voluptatum dolorem
      provident dolor beatae aut ut mollitia ullam. Lorem ipsum dolor sit amet
      consectetur adipisicing elit. Vero deleniti veritatis labore molestiae
      architecto aspernatur esse ipsam placeat velit natus quisquam error, dicta
      doloremque exercitationem optio? Minus numquam accusamus veritatis unde
      aspernatur accusantium qui, voluptate officiis possimus dolore inventore
      nostrum aliquam voluptatum dolorem provident dolor beatae aut ut mollitia
      ullam.re nostrum aliquam voluptatum dolorem provident dolor beatae aut ut
      mollitia ullam. Lorem ipsum dolor sit
      <span><button @click="scrollX(100)">scroll 300</button></span>
    </p>
  </div>
</template>

<script>
export default {
  methods: {
    // to demonstrate vue native version of dom handling using refs
    scrollX(x) {
      this.$refs.paraRef.scrollLeft += x;
      console.log(this.$refs.paraRef.scrollLeft)
    }
  }
}
</script>

<style scoped>
#subcomp {
  overflow: scroll;
  border: 1px solid black;
  width: 100vw;
  height: 150px;
  background: #eee;
}
#para {
  width: 200vw;
}
</style>
