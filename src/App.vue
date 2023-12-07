<script setup>
import { ref } from 'vue'
import child from './components/Child.vue'
import slots from './components/Namedslot.vue'
  
const message = ref('hello')
let arr = ['hello world', 'Namastee duniya ']

function call(e){
    alert(e)
}

</script>

<template>
<child v-model="message" :data="arr" @events="(e)=>call(e)"/> {{ message }}
<slots>
  <template #header>
      <h1 >Names slots starts here </h1>
    </template>

    <template #default>
      <p>A paragraph to default view</p>

    </template>

    <template #footer>
      <h3>Names slots Ends here</h3>
    </template>
</slots>

<button @click="alert('hello')">Clickme</button>


</template>


