<template>
  <div id="app">
    <h1>Belajar Vue bersama {{namaku}}</h1>
    <FormBelajar id="forml" pesan="Ayo kita belajar vue" :nama="nama"/>
    <FormBelajar2 id="formr" :gantinm="gantiNama" />
    
  </div>
</template>

<script>
import FormBelajar from './components/FormBelajar.vue'
import FormBelajar2 from './components/FormBelajar2.vue'

export default {
  name: 'app',
  components: {
    FormBelajar,
    FormBelajar2
  },
  data : function(){
    return {
      nama : "fahrul",
    }
  }, 
  computed:{
      namaku: function(){
          return "ini Namaku : " + this.nama;
      },
  },
  methods:{
    gantiNama(nama){
      this.nama = nama;
    }
  }
}
</script>

<style>
#formr {
  float:right
}
#forml {
  float: left;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  padding: 90px;
}
</style>
