<template>
    <div>
        <div class="container">
            <div v-for= "(element, index) in liDischi" :key="index" class="box-container">

            </div>
        </div>

    </div>
</template>
<script>
import axios from "axios";

export default {
    data (){
        return{
            liDischi: []

        }

    },


    mounted(){
    axios.get('https://flynn.boolean.careers/exercises/api/array/music')
    .then((musica)=>{
        this.liDischi = musica.data.response.slice(),
        console.log(this.liDischi)
    } )
        
    
    },
    
}
</script>


<style>
.box-container{
    width: 40px;
    height: 60px;
    background-color: grey;
}

</style>
   

    
      
      

      

  

      






