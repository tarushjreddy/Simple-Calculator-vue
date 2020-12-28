<template>
<div>
<AppHeader />
<div class="Orient">
<Calculator/>
</div>
</div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

import AppHeader from './App_header.vue';
import Calculator from './calculator.vue';

export default {
  components:{
    AppHeader,
    Calculator
  }
  
}
</script>

<style>
body{
  margin: 0px;
}
.Orient{
  display: flex;
  justify-content: center;
  margin-top: 200px;
}

</style>
