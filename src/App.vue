<template>
  <div id="app">
    Vue JS LifeCycle (Yaşam Döngüsü Methodları)
    <input class="input" v-model="text">
    {{ text }}
    <button  onclick="destroy()">Destroy</button>

  </div>
</template>



<script  >

export default {
  name: 'App',
  data() {
    return {
      text: ""
    }
  },
  methods: {
    destroy() {
      console.log("Destroy method called");
    }
  },
  beforeCreate() {
    console.log("WORKS BEFORE VUE CREATION")
    // Vue oluşturulmadan önce çalışır.
  },
  created() {
    console.log("VUE HAS BEEN CREATED")
    // Vue oluşturuldu 
    //vue has been created (servis isteklerini atabiliriz)
  },
  mounted() {
    console.log("VUE CREATED AND CONNECTED TO DOM")
    //Vue oluşturuldu ve doma bağlandı
    //vue has been created (servis isteklerini atabiliriz)

  },
  beforeUpdate() {
    console.log("BEFORE DOM WAS UPDATED")
    // Dom güncellenmeden önce 
  },
  updated() {
    console.log("RENDERED TO DOM")
    //Dom'a render edildi
  },
  beforeDestroy() {
    console.log("BEFORE IT WAS DESTROYED")
    //Yok edilmeden önce
  },
  destroyed() {
    console.log("AFTER İT WAS DESTROYED")
    //Yok edildikten sonra
  },



}

</script>






<style scoped>

#app {
  width: max-content;
  justify-content: center;
  align-items: center;
  align-content: center;

}

.input {
  border-radius: 40px;
  height: 1cm;
  margin-left: 10px;
}

#button {
  width: 70px;
  height: 30px;
  border-radius: 50px;
}
</style>
