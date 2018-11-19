<template>
    <!-- <form v-on:submit.prevent> -->
    <div>
        <h2>Form 1 : {{nama}} </h2>
        <input type="text" v-model="hasil" placeholder="nama">
        <input type="text" id="inputan" placeholder="nama">
        <button v-on:click="gantiHasil2">Test</button>
        <h3>Hasil : {{hasil}}</h3>
        <h3>Hasil 2 : {{hasil2}}</h3>
    </div>
    <!-- </form> -->
</template>
<script>
export default {
  name: 'FormBelajar',
  props:[
      'nama',
      'pesan'
  ],
  data: function(){
      return {
          hasil:"Default",
          hasil2:"",
      }
  },
  methods:{
      gantiHasil2(){
          this.hasil2 = document.getElementById('inputan').value;
      }
  }
}
</script>
<style scoped>

</style>
