<template>
  <div id="app">
    <template>
      <v-button-navigation v-model="value">
        <v-btn value ="recent" @click="gotoHome()">
          <span>HOME</span>

          <v-icon>mdi-home-variant-outline</v-icon>
    </v-btn>

      <v-btn value ="recent" @click="gotoPage2()">
         <span>PROFILE</span>

          <v-icon>mdi-account-circle</v-icon>
     </v-btn>

     <v-btn value ="recent" @click="gotoPage3()">
         <span>CONTACT</span>

          <v-icon>mdi-card-account-mail-outline</v-icon>
     </v-btn>

     <v-btn value ="recent" @click="gotoPage4()">
         <span>PROJECT</span>

          <v-icon>mdi-file-sign</v-icon>
     </v-btn>

      </v-button-navigation>
    </template>
    <router-view />
  </div>
</template>

<script>
export default {
   name: 'App',
  methods: {
    gotoHome(){
      if(this.$route.path !== '/'){
        this.$router.push('/')
      }
    },
    gotoPage2(){
       if(this.$route.path !== '/page2'){
          this.$router.push('/page2')
      }
    },
    gotoPage3(){
       if(this.$route.path !== '/page3'){
          this.$router.push('/page3')
      }
    },
    gotoPage4(){
       if(this.$route.path !== '/page4'){
          this.$router.push('/page4')
        }
     }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 20px;
}
.router-link-exact-active {
  color: blue;
}
</style>