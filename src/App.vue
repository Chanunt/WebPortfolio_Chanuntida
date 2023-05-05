<template>
  <div id="app">
   <template>
      
      <v-bottom-navigation v-model="value">
        <v-btn value="Profile" @click="goToHome()">
          <router-link to="/">Profile</router-link> 

          <v-icon> mdi-account-box-outline</v-icon>
        </v-btn>
        

        <v-btn value="Contact" @click="goToPage2()">
          <router-link to="/Contact">Contact</router-link>

          <v-icon>mdi-card-account-phone-outline</v-icon>
        </v-btn>

        
        <v-btn value="Project" @click="goToPage3()">
          <router-link to="/Project">Project</router-link> 

          <v-icon>mdi-animation-outline</v-icon>
        </v-btn>
      </v-bottom-navigation>
</template>
    <router-view />
  </div>
</template>

<script>
export default {
   name: 'App',

   data: () => ({
      //
   }),
   methods: {
     goToHome(){
       this.$router.push('/');
     },
     goToPage2(){
       this.$router.push('/Contact');
     },
     goToPage3(){
       this.$router.push('/Project');
     },
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
  margin-top: 60px;
}
.router-link-exact-active {
  color: blue;
}
</style>