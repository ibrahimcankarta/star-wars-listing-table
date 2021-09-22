<template>
     <div>
       <h1 class="font-bold text-2xl text-indigo-600 flex justify-center">-Star Wars Listing Table- </h1>
     </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'mainComponent',
  components: {
  },
  data () {
    return {
      type: 'table',
      dataSet: [],
    }
  },
  mounted: function() {
    console.log(this.checkedFilters)
    axios.get('https://swapi.dev/api/people/')
      .then(response => {
        this.dataSet = response.data;
      })
      .catch(error => {
        console.log(error);
      });
  },
  methods: {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
