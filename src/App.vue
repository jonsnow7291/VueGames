<template>
  <div>
    <h1>holi {{vue}}</h1>
    <h2 v-bind:style="colorh2">{{ arrray}}</h2>
    <p v-if="bool===true">menas</p>
    <p v-else-if="bool===false">adios</p>
    <p v-else="">no lo se , NO LO SE!!!</p>
    <ul>
      <li v-for="(palabras, index) in arrray"
      :key="index"
          >
          {{index}} - {{ palabras }}
      </li>
    </ul>
    <ul>
      <li v-for="(games, propiedad) in juegos"
      :key="games.name">
          {{propiedad}} : {{ games.name }}- {{ propiedad }}:{{ games.category }} - {{propiedad}}:{{ games.plataform }}
      </li>
    </ul>
  </div>
</template>

<style>
  h1 {
    color: red;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  }
</style>
<script setup>
    const juegos =
    [{"name":"Dark souls",
      "category":"Action",
      "plataform":"PS5"
    },{"name":"Forza Horizon",
      "category":"Cars",
      "plataform":"XBOX"
    },{"name":"Tomb Raider",
      "category":"Action",
      "plataform":"PC"
    }]
    const bool = "carne";
    const vue ="Vue Dynamic";
    const colorh2 = "color:orange"
    const arrray = ["buenos", "dias", "COMO ESTAS"]
</script>