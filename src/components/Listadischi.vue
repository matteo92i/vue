<template>
    <div>
        <div class="container">
            <div v-for= "(element, index) in liDischi" :key="index" class="box-container">
                <img class="dimensione" :src="element.poster" :alt="element.author">
                <h4>{{element.title}}</h4>
                <p>{{element.author}}</p>
                <p>{{element.year}}</p>

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
.container{
    width: 1000px;
    height: 800px;
    margin: 0 auto;
    background: grey;
    display: flex;
    flex-wrap: wrap;
}
.box-container{
    width: 200px;
    height: 90px;
    background-color: grey;
    margin-bottom: 5px;

}
.dimensione{
    width: 90%;
    height: auto;
}

</style>
   

    
      
      

      

  

      






