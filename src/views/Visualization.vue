<template>
  <div id="visualization">
   
  </div>
</template>

<script>

export default {
    name: 'Visualization',
    components: {

    },
    computed: {
      checkIfSplashIsRendered() {
          return this.$store.state.splashRenderedOnInitialLoad;
      }
    },
    mounted(){
      const self = this;
      
    },
    updated(){
      this.lazyLoadImages();
    },
    methods:{
    }
} 
</script>

<style lang="scss">
//Hides v-img title element
.title-v-img{
  display: none;
}
</style>
