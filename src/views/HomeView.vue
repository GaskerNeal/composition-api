<template>
<div class="home">
  <h1>Home Page</h1>
  <p>Hello {{name}}. I am {{age}} years old.</p>
  <input type="text" v-model="name">
  <button @click="handleClick">Click</button>
  <button @click="age++">Increase Age</button>
</div>
</template>

<script>
import { ref } from '@vue/reactivity';
// @ is an alias to /src

export default {
  setup() {
    let name = ref("MMS");
    let age = ref(20);
    let handleClick = () => {
      name.value = "KZO"
    }
    return {name, age, handleClick};
  }
}
</script>
