<template>
<div style="color: white">
  <Particles
      id="tsparticles"
      :particlesInit="particlesInit"
      :particlesLoaded="particlesLoaded"
      url="http://foo.bar/particles.json"
  />
  <a href="#middle">Middle</a>
  <div v-for="n in 1000" :key="n" >{{n}}</div>
  <div v-for="a in 1000" :key="a" id="middle"  >
    <a ></a>{{a}}</div>
<!-- <v-row>-->
<!--   <v-col cols="4" class="text-center">a</v-col>-->
<!--   <v-col cols="4" class="text-center">b</v-col>-->
<!--   <v-col cols="4" class="text-center">c</v-col>-->
<!--   <v-col cols="4" class="text-center">c</v-col>-->
<!--   <v-col cols="4" class="text-center">c</v-col>-->
<!--   <v-col cols="4" class="text-center">c</v-col>-->
<!--   <v-col cols="4">c</v-col>-->
<!--   <v-col cols="4">c</v-col>-->
<!--   <v-col cols="4">c</v-col>-->
<!--   <v-col cols="4">c</v-col>-->
<!--   <v-col cols="4">c</v-col>-->
<!--   <v-col cols="4">c</v-col>-->
<!--   <v-col cols="4">c</v-col>-->
<!--   <v-col cols="4">c</v-col>-->
<!--   <v-col cols="4">c</v-col>-->
<!--   <v-col cols="4">c</v-col>-->
<!--   <v-col cols="4">c</v-col>-->
<!--   <v-col cols="4">c</v-col>-->
<!-- </v-row>-->
</div>
</template>

<script>

export default {
  name: "test"
}
</script>

<style scoped>

</style>