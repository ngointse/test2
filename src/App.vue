<template>
  <v-app>
    <v-app-bar
      app
      height="80"
      color="#473B5B"
      dark
    >
      <div class="d-flex align-center">
        <v-menu offset-y v-if="$vuetify.breakpoint.smAndDown">
          <template v-slot:activator="{ on, attrs }">
            <v-btn
                dark
                icon
                v-bind="attrs"
                v-on="on"
            >
              <v-icon>
                mdi-menu
              </v-icon>
            </v-btn>
          </template>
          <v-list>
            <v-list-item
                @click="$router.push({name:item.value})"
                v-for="(item, index) in items"
                :key="index"
            >
              <v-list-item-title>{{item.title }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
<!--        <div v-else>False</div>-->
      </div>
      <v-spacer></v-spacer>
      <template v-if="!$vuetify.breakpoint.smAndDown">
           <a href="#test">Go To Middle</a>
              <div class="px-5 " @click="$router.push({name:'home'})">Home</div>
              <div  class="px-5 " @click="$router.push({name:'test'})">Test</div>
              <div  class="px-5 " @click="$router.push({name:'about'})">about</div>
      </template>

    </v-app-bar>
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',
  data: () => ({
    //
    items: [
      { title: 'Home',value:'home' },
      { title: 'Test',value:'test' },
      { title: 'About' ,value:'about'},
    ],
  }),
};
</script>

<style>
.whiteCol{
  color: #ffffff;
}
#app{
  background: #1D0731;
}
</style>
