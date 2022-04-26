<template>
  
<div>
  <h3>Control de Flujo Másico</h3>
    <button @click="temperatura--">Disminuir</button>
    <span>{{temperatura}}</span><span> °C</span>
    <button @click="temperatura++">Aumentar</button>
  </div>
</template>

<script>
  export default {
    data(){
      return {
        temperatura: 10,
        humedad: 0,
      }
    }
  }
</script>
