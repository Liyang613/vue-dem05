<template>
  <div class="inputA">
      <input type="text" @focus="fn" v-model="msg"><button>搜索</button>
  </div>
</template>

<script>
export default {
  name: 'inputA',
  data() { 
    return {
   msg:""
    }
  },
  props: {

  },
  components:{
  },
  mounted() {
   $bus.$on("toinput",(val)=>{
     this.msg=val
     this.$emit("change",false)
   })
  },
  methods:{
   fn(){
     this.$emit("change",true)

   }
  },
 }
</script>

<style lang="scss">
li{
    width: 100%;
    height:40px;
}
 
</style>