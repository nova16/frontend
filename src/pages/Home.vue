<template>
  <h1>Hello World</h1>
    <h4>Project Vue Pertama Saya</h4>
    <h4>Nama Saya {{ nama }}</h4>
    <h4>Umur Saya {{ tahunlahir }} tahun</h4>
    <input v-model="kotalahir" />  
    <h5>Kota Lahir Saya :  {{ kotalahir }} </h5>
    <button v-on:click="next">Next</button>
</template>

<script>
export default {
    data(){
        return{
            nama : "Nova Agustina",
            tahunlahir : 1993,   
            kotalahir : "Bandung"
        }
    },
      methods:{
        next(){
            this.tahunlahir += 1;
        }
    },
    mounted(){
        this.tahunlahir = 2021 - this.tahunlahir;        
    }
}
</script>