<template>
  <v-app>
    
    <v-main >
      
      <men></men>
  
      <!-- <cal></cal>
      <car></car>
      <divi></divi>
      <caro></caro> -->
      
     </v-main>
     <router-view></router-view>
     
   </v-app>
   
</template>


<script>
import  men from './components/MenuUno.vue';

export default {
  name: 'App',

  components: {
    men
    
  },

  data: () => ({
    //
  }),
};
</script>
