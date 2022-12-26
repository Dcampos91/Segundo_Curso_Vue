<template>
  <h2>Coche - CarOptions API</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p> 
  <p>Potencia: {{ power }}</p>
  
  <button @click="upPower">Aumentar Potencia</button>
  <button @click="upPower10(10)">Aumentar Potencia x10</button>
  <button @click="downPower">Disminuir Potencia</button>
  <button @click="Reset">Potencia Original</button>
</template>

<script>
export default {
  data(){
    return{
      brand: "Seat",
      model:"Leon",
      power:50,
    };
  },
  methods:{
    upPower10(newPower){
      this.power = this.power + newPower;
    },
    upPower(){
      this.power++;
    },
    downPower(){
      this.power--;
    },
    Reset(){
      this.power = 50;
    },
  }
};
</script>

<style>

</style>