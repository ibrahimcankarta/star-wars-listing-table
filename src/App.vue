<template>
  <div id="app">
    <MainComponent/>
  </div>
</template>

<script>
import MainComponent from './components/mainComponent.vue'
export default {
  name: 'App',
  components: {
    MainComponent
  }
  /*async created() {
    var { data }=await axios.get("https://swapi.dev/api/people/") ;
    console.log(data)
  }*/
}
</script>

<style>

</style>
