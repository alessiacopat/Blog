<template>
  <div>
    <app-header v-bind:title="title" v-on:changeTitle="updateTitle($event)"></app-header>

    <!-- "ninjas" fa riferimento alla props nel file Ninjas.vue -->
    <app-ninjas v-bind:ninjas="ninjas"></app-ninjas>

    <app-footer v-bind:title="title"></app-footer>
  </div>
</template>

 

<script>

  import Header from './components/Header.vue';
  import Footer from './components/Footer.vue';
  import Ninjas from './components/Ninjas.vue';

  export default {
    components: {
      'app-header': Header,
      'app-footer': Footer,
      'app-ninjas': Ninjas
    },
    data () {
      return {
         ninjas: [
            {name: 'Ryu', speciality: 'Vue Components', show:false},
            {name: 'Crystal', speciality: 'HTML Wizardy', show:false},
            {name: 'Hitoshi', speciality: 'Click Events', show:false},
            {name: 'Tango', speciality: 'Conditionals', show:false},
            {name: 'CrysKamital', speciality: 'Webpack', show:false},
            {name: 'Yoshi', speciality: 'Data Digging', show:false}
        ],
        title: "Vue ninjas"
      }
    },
    methods: {
      updateTitle: function(updatedTitle){
        this.title = updatedTitle;
      }
    }
  
  }
</script>

<style scoped>
  h1{
    color:purple;
  }
</style>
