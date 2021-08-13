<template>
  <div id="app" class="text-center ml-4">
    <h1 class="py-3">Crear nueva tarea</h1>
    <label class="pr-4">Tarea</label>
    <input class="me-4 ms-4" type="text" v-model= "Actividad" placeholder="Ingrese nueva tarea" />
    <button @click="AgregarLista">Agregar</button>
    <ul>
      LISTA 
      <li v-for= "(Tarea, index) of Tareas" :key="index">
        {{Tarea}}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "app",
  data: () => ({
    Actividad: "",
    Tareas: ["Comprar cigarros", "Volverme un concepto"]
  }),
  methods:{
    AgregarLista: function(){
      this.Tareas.push(this.Actividad)
      this.Actividad = "";
    }
  }
};
</script>
<style scoped>
body,html{
  width: 100%;
  height: 100%;
}
div{
  background-color: rgb(255, 181, 203);
  margin: 70px;
  width: 1000px;
  height: 500px;
  border-radius: 10%;
}

h1 {
  color: rgb(231, 94, 167);
}
button {
  width: 150px;
  height: 45px;
  border-radius: 10%;
  background-color: rgb(251, 164, 164);
  color: teal;
  border-color: aqua;
  font-family: monospace;
  font-size: 12px;
  font-weight: 600;
}

input {
  background-color: paleturquoise;
  color: violet;
  width: 400px;
}
label {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  color: royalblue;
  font-weight: 600;
  font-size: 30px;
}

ul {
  padding-right: 30px;
  font-weight: 600;
}
li{
  color:royalblue;
  font-family: monospace;
}
</style>
