<template>

    <div>
        <h2>Form 2</h2>
        <input type="text" v-model="dataToPass">
        <!-- {{dataToPass}} -->
        <button @click="kirimData">Kirim</button>
    </div>
</template>
<script>
export default {
  name: 'FormBelajar2',
  props:[
      'gantinm'
  ],
  data: function(){
      return {
          dataToPass:'',
          dataPass:{
              satu:'dasds',
              dua:'dad'
          }
      }
  },
  watch:{
      dataToPass:function(val,oldval){
        console.log(oldval + ' Berubah menjadi '  + val);
      },
      'dataPass.satu':function(){
          
      }
  },
  methods:{
      kirimData(){
          this.gantinm(this.dataToPass);
      }
  }
}
</script>
<style scoped>

</style>
