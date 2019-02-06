<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Halo dunia"/> -->
    <h1>{{ nama }}</h1>
  <h2>Nama : <input v-model="nama" type="" name=""><br></h2>
  <h2>Nilai Anda : {{  nilai }}</h2>
  <button @click = "totalnilai">Click Me</button>
  <h2>1. Siapa Presiden Amerika Serikat Saat Ini ?</h2>
  <input type="radio" name="" v-model="soal1" value="Obama">Barrack Obama
  <input type="radio" name="" v-model="soal1" value="George Washington">George Washington
  <input type="radio" name="" v-model="soal1" value="Abraham Lincoln">Abraham Lincoln
  <input type="radio" name="" v-model="soal1" value="Trump">Donald Trump<br>
  <h2>2. Apakah arti "ПРИВЕТ" Dari Bahasa Rusia ?</h2>
  <input type="radio" name="" v-model="soal2" value="Halo">Halo
  <input type="radio" name="" v-model="soal2" value="Dadah">Dadah
  <input type="radio" name="" v-model="soal2" value="Selamat Malam">Selamat Malam
  <input type="radio" name="" v-model="soal2" value="Selamat Makan">Selamat Makan<br>
  <h2>3. Siapakah Presiden Pertama Indonesia ?</h2>
  <input type="radio" name="" v-model="soal3" value="Soekarno">Soekarno
  <input type="radio" name="" v-model="soal3" value="Habibie">B.J Habibie
  <input type="radio" name="" v-model="soal3" value="Megawati">Megawati Soekarnoputri
  <input type="radio" name="" v-model="soal3" value="Abdurrahman Wahid">Abdurrahman Wahid<br>
  </div>
</template>

<script>
/*import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  }
}*/
export default{
  name: 'App',
  data() {
    return{
      nama: '',
      nilai: 0,
      soal1: '',
      soal2: '',
      soal3: ''
    }
},
methods: {
    totalnilai(){
      if(this.soal1 == 'Trump' && this.soal2 == 'Halo' && this.soal3 == 'Soekarno') {
        this.nilai=+3
      }
      else if (this.soal1 == 'Trump' && this.soal2 == 'Halo') {
        this.nilai=+2
      }
      else if (this.soal1 == 'Trump' && this.soal3 == 'Soekarno') {
        this.nilai=+2
      }
      else if (this.soal2 == 'Halo' && this.soal3 == 'Soekarno') {
        this.niali=+2
      }
      else if (this.soal1 == 'Trump') {
        this.nilai=+1
      }
      else if (this.soal2 == 'Halo') {
        this.nilai=+1
      }
      else if (this.soal3 == 'Soekarno') {
        this.nilai=+1
      }
      else{
        this.nilai = 0
      }
    }
  }
}
</script>


<style>
#app {
  font-family: 'AveHelloWorldnir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
