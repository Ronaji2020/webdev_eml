<template>
  
<div>
  <h4>Control de Temperatura</h4>
  <button @click="temperatura--">Disminuir</button>
   <span 
      :class="{
        warning : temperatura > 20 && temperatura < 25, 
        danger : temperatura >= 25}" >

        {{temperatura}}</span><span> °C</span>
                            <button @click="temperatura++">Aumentar</button>
    <br>
    <h5 v-if="temperatura > 20" style="color:orange">Cuidado!</h5>
    <h5 v-show="temperatura > 25" style="color:red">Mucho Cuidado!</h5>
    <br><br>

    <h4>Control de humedad</h4>
    <button @click="humedad--">Disminuir</button>
    <span>{{humedad}}</span><span> %</span>
    <button @click="humedad++">Aumentar</button>
    <br><br>


    </div>
    </template>

<script>
export default {
    data(){
        return{
            temperatura: 10,
            humedad: 0
        }
    }
}
</script>

<style>
  .tipografia{
    font-family: Arial;
  }
  .warning{
    color:rgb(198, 140, 16)
  }
  .danger{
    color: red
  }
</style>


