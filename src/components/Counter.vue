<template>
  <h2>{{ title }}</h2>
  <p>{{ counter }} <sup> 2 </sup> = {{ GetSquare }}</p>
  <div style="background-color: blue">
    <button @click="decreaseAccount">-1</button>
    <button @click="increaseAccount">+1</button>
  </div>
</template>

<script>
export default {
  props: ["title"],
  //La data es donde se van a crear las variables que van a hacer funcionar nuestro sistema, pueden ser objetos, int, string, etc.
  data() {
    return {
      counter: 0,
    };
  },
  //Los metodos son las acciones que se ejecutan con todas las variables que intervienen en el codigo
  methods: {
    increaseAccount() {
      this.counter++;
    },
    decreaseAccount() {
      this.counter--;
    },
  },
  //La propiedad computada es la operacion que se va a ejecutar, la operacion que requiera procesamiento
  computed: {
    GetSquare() {
      return this.counter * this.counter;
    },
  },
};
</script>

<style>
button {
  background-color: cadetblue;
  border-radius: 10px;
  border: 1px solid white;
  color: aliceblue;
  cursor: pointer;
  margin: 0 5px;
  padding: 5px 15px;
  transition: 0.3s ease-in-out;
}
</style>


