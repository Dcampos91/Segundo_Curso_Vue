<template>
  <h2>Coche - CarComposition API</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ power }}</p>
  <!-- <p>Color: 
    <ul>
        <li v-for="(color,index) in colors" :key="index">
            {{ index }}: {{ color }}
        </li>
    </ul>
  </p>
  <p>Precio: $ {{ price }}</p>
  <p>Potencia: {{ power }} CV</p>
  
  {{ mensaje.title }} {{ mensaje.text }} -->
  <!--<ul>
    <template v-for="(power,index) in powers" :key="index">
        <li v-if="power < 280">
        Urbana: {{ power }}
        </li>
        <li v-else-if="power === 280">
        Hibrido: {{ power }}
        </li>
        <li v-else>
        Carrera: {{ power }}
        </li>
    </template>
  </ul>
  <p>Potencias Urbanas menor a 300 cv</p>
  <ul>
    <template v-for="(power,index) in powers" :key="index">
        <li v-if="power < 300">
        {{ power }}
        </li>
    </template>
  </ul>
  <p>Potencias Urbanas mayores a 300 cv</p>
  <ul>
    <template v-for="(power,index) in powers" :key="index">
        <li v-if="power >= 300">
        {{ power }}
        </li>
    </template>
  </ul>
  <p>Potencia: {{ power }}</p>-->
  
  <button @click="upPower">Aumentar Potencia</button>
  <button @click="upPower10(10)">Aumentar Potencia x10</button>
  <button @click="downPower">Disminuir Potencia</button>
  <button @click="resetPower">Potencia Original</button>
  
</template>

<script>
import { ref } from "vue";
export default {
// setup() {
//    const brand = "Audi";
//    const model = "A4";
//    const colors = ["Azul","Rojo","Verde","Amarillo"];
//    const price = 4500;
//    const power = 240;
//    const mensaje = {
//        title: "hola mundo",
//        text: "Adios",
//    };
//    return{
//        brand,
//        model,
//        colors,
//        price,
//        power,
//        mensaje,
//    }; 
// },
 setup(){
    const brand = "Audi";
    const model = "A4";
    //const powers = [60, 80, 120, 160, 200, 280, 300, 390, 540, 500];
    let power = ref(40);
    const resetPower = () => {
      power.value = 40;
    };
    const upPower = () => {
      power.value ++; 
    };
    const upPower10 = (newPower) => {
      power.value = power.value + newPower; 
    };
    const downPower = () => {
      power.value --;
    };
    return{
        brand,
        model,
        power,
        upPower,
        downPower,
        resetPower,
        upPower10,
    };
 },     
};
</script>

<style>

</style>