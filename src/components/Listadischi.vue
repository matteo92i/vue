<template>
    <div>
        <div class="container">
            <div class="box-container"></div>
        </div>

    </div>
</template>
<script>
import axios from "axios";

export default {
    data


    mounted(){
    axios.get('https://flynn.boolean.careers/exercises/api/array/music')
    .then(risposta)
    console.log(risposta)
    },
}
</script>


<style>

</style>
   

    
      
      

      

  

      






