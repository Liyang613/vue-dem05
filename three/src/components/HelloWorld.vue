<template>
  <div class="hello">
        <inputA @change="cfn"></inputA>
        <Searchlist  v-show="a"></Searchlist>
  </div>
</template>

<script>
import inputA from "../components/inputA"
import Searchlist from "../components/searchlist"
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      a:false
    }
  },
  components:{
    inputA,
    Searchlist,
  },
  methods:{
    cfn(val){
       this.a=val
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
