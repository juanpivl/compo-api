<template>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
</template>


<script>
import { onBeforeMount,onMounted,
onUpdated,
onUnmounted,
onBeforeUpdate,
onErrorCaptured,
onRenderTracked,
onRenderTriggered,
onActivated,
onDeactivated,
onServerPrefetch, } from '@vue/runtime-core'
  export default{
    setup(){
      onBeforeMount(()=>{
        console.log('onbeforeMount')
      })
      onMounted(()=>{
        console.log('onMount')
      })
      onUpdated(()=>{
        console.log('onupdated')
      })
      onUnmounted(()=>{
        console.log('onunMount')
      })
      onBeforeUpdate(()=>{
        console.log('onbeforeupdate')
      })
      onErrorCaptured(()=>{
        console.log('onerror capture')
      })
      onRenderTracked(()=>{
        console.log('render trackerd')
      })
      onRenderTriggered(()=>{
        console.log('render trigerred')
      })
      onActivated(()=>{
        console.log('onactivated')
      })
      onDeactivated(()=>{
        console.log('ondesactivate')
      })
      onServerPrefetch(()=>{
        console.log('oserverprefecth')
      })
    },
  }

</script>