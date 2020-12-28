<template>
    <div class="outline_cal">
        <p class="result">{{calulation}}</p>
       <div class="numbers">
        <button @click="pressed('1')">1</button>
        <button @click="pressed('2')">2</button>
        <button @click="pressed('3')">3</button>
        <button @click="pressed('4')">4</button>
        <button @click="pressed('5')">5</button>
        <button @click="pressed('6')">6</button>
        <button @click="pressed('7')">7</button>
        <button @click="pressed('8')">8</button>
        <button @click="pressed('9')">9</button>
        <button @click="pressed('0')">0</button>
        <button @click="pressed('=')">=</button>
        <button @click="pressed('clear')">CAL</button>
        </div>
    </div>
</template>
<script>
import {ref} from "vue";
export default {
    setup(){
const calulation = ref('');
const operations = ['+','-', '/', '*'];
function pressed(value){
    if (value === '=') cal(value);
    else if(operations.includes(value)) applyOperation(value);
    else appendNumbber(value);
    calulation.value = calulation.value+ value
}
function appendNumbber(value){
   calulation.value = calulation.value+ value  

}
function applyOperation(value){
return value;
}
function cal(value){
    return value;
    
}
return {calulation, pressed}; 
    }
}
</script>
<style >
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@500&display=swap');
.result{

    height: 50px;
    /* border: 1px solid black; */
    padding: 20px;
    text-align: right;
    max-width: 360px;
    font-size: 30px;
    font-family: 'Poppins', sans-serif;
}
.numbers > button{
    height: 90px;
    font-size: 23px;
    width: 90px;
    outline: none;
    border: none;
    margin: 5px;
    border-radius: 50px;
    transition: all 200ms ease-in-out;
    font-family: 'Poppins', sans-serif;

}
.numbers > button:hover{
    background-color: gray;
    

}

.numbers{
    max-width: 400px;
    flex-wrap: wrap;
    font-family: 'Poppins', sans-serif;
  
}
.outline_cal{
    height: 100%;

    min-width: 500px;
    font-family: 'Poppins', sans-serif;
}
</style>