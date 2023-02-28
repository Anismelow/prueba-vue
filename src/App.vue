<script setup>
let nombre = "Anyell Mendoza"
let colorstyle = "color: purple";
let arrayColores = ["red", "green", "blue"];
const arrayFrutas = ["🍎", "🍌", "🍉", "🍓", "🍒"];
const arrayFruta = [
        {
            name: "Manzana",
            price: "$1.00",
            description: "Una manzana",
        },
        {
            name: "Pera",
            price: "$2.00",
            description: "Una pera",
        },
        {
            name: "Naranja",
            price: "$3.00",
            description: "Una naranja",
        },
    ];

let objetoFruta =  {
            name: "Manzana",
            price: "$1.00",
            description: "Una manzana",
        }

let activo = true;

</script>

<template>
  <h1>hola soy {{ nombre.toLocaleUpperCase() }}</h1>

  <h2>estos son los coleres primarios {{ arrayColores }}</h2>

 <ul>
    <li v-for="colores in arrayColores">
      {{ colores.toLocaleUpperCase() }}
    </li>
 </ul>

 <h2 :style="`color: ${arrayColores[1]}`">soy verde</h2>

 <h2>{{ activo ? 'Estoy activo' : 'Estoy inactivo' }}</h2>

 <p v-if="activo === true">estoy activo</p>

 <p v-else-if="activo === false">estoy estoy inactivo </p>

 <p v-else>estoy indeciso</p>

 <h2 v-show="false">hola, estoy descubierto</h2>

 <ul>
    <li v-for="(fruta,index) in arrayFrutas" :key="index">
      {{ fruta }}
    </li>
 </ul>

 <ul>
    <li v-for="frut in arrayFruta" :key="arrayFruta.name">
      {{ frut.name }}, {{ frut.price }}, {{ frut.description }} 
    </li>

    {{ objetoFruta }}
 </ul>

 <ul>
    <li v-for="(value,propiedad, index ) in objetoFruta" :key="value">
    {{ index }} - {{ propiedadd }} : {{ value }}, 
    </li>
 </ul>
</template>

<style>
h1{
  color: red;
}
</style>