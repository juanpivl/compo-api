<template>
  <div class="home">
    <h1>Reactive vs Ref</h1>
    <h3>{{ ironman }}</h3>
    <h3>{{ hulk }}</h3>
    <button @click="changeIronman">cambiar iron man</button>
    <button @click="changeHulk">Cambiar hulk</button>

    <h3>Ironman: {{ ironmanIsAlive }}</h3>
    <h3>Hulk: {{ hulkIsAlive }}</h3>
    <button @click="changeStatus">change status </button>

  </div>
</template>

<script>
import {ref,reactive} from 'vue'


export default {
  name: 'HomeView',
  setup(){
    const ironman = ref({name: 'tony', age:50})
    const hulk = reactive({name: 'bruce', age:40})

   const ironmanIsAlive = reactive(false)
    const hulkIsAlive = ref(true)

    const changeStatus = () =>{
      hulkIsAlive.value = !hulkIsAlive.value
      //ironmanIsAlive =reactive(!ironmanIsAlive)
    }

    return{
      ironman,
      hulk,

      ironmanIsAlive,
      hulkIsAlive,

      changeStatus,
      changeIronman: ()=>{
        ironman.value.name = 'Tony Stark'
        ironman.value.age = '90'
      },
      changeHulk: ()=>{
        hulk.name = 'Bruce banner'
        hulk.age = '3214'
      },
    }
  }
}
</script>
