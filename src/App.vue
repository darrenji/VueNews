<template>
    <div class="container">
        <source-selection v-on:sourceChanged="sourceChanged"></source-selection>
        <news-list v-bind:source="source"></news-list>
   
    </div>
</template>

<script>
    import SourceSelection from './components/SourceSelection.vue'
    import Newslist from './components/Newslist.vue'
    
    import Test from './components/Test.vue'
   
    export default {
      data () {
        return {
          source: ""
        }
      },
      components: {
          newsList: Newslist,
          sourceSelection: SourceSelection,
          appTest:Test
      },
      methods: {
          sourceChanged: function(source){
              this.source = source;
          }
      }
    }
</script>

<style>

</style>
