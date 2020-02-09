<template>
  <div class="searchlist">
      <ul>
          <li v-for="(item,index) in arr"  :key="index" @click="toinput(item)">
             {{item}}
          </li>
      </ul>
  </div>
</template>

<script>
export default {
  name: 'Searchlist',
  data() { 
    return {
      arr:["熊大","熊二","小熊"],
    }
  },
  props: {

  },
  components:{
  },
  mounted() {

  },
  methods:{
   toinput(val){
     $bus.$emit("toinput",val)
   }
  },
 }
</script>

<style>
li{
    border: 1px solid red;
}
</style>