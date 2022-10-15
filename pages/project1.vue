<template>
  
  <div>

    <div class="title">
    Objects in Time
    </div>

  <div class="video">
  <b-embed
    type="iframe"
    aspect="16by9"
    src="https://www.youtube.com/embed/zpOULjyy-n8?rel=0"
    allowfullscreen
  ></b-embed>
   </div>

<b-row class="description" >
  <b-col md="4">
   <p>Individual Project</p> <br /> 

   <p>Time: June 2022</p> <br /> 

   <p>Tool: Lens Studio</p> <br /> 
  </b-col>

  <b-col md="8" >
    <h2 class="info">
      A AR Lens which allows you to scan an object in your home and explore what the object was like in the past.
    </h2>
    <br /> 
    <div class="long-info">
      When you enter this Lens, first there will be a hint that tells you to look for a mug, bottle, phone, or shoe. When you find one of the objects and tap the screen, the related historical artifact and its description will appear. You will be able to drag and place the artifact on any surface, as well as rotating and scaling. After you finish exploring the current item and turn your phone away from it, the contents will disappear for the next scan. with this lens, You can see how everyday items evolve over time and learn about culture and history in a fun and intuitive way.

    </div>
  </b-col>
  </b-row>
  </div>


  


 

</template>

<script>
export default {
  data(){
    return{
      name:"sihan website",
    }
  }

}
</script>

<style scoped>
.title{
  position: relative;
  left: 100px;
  width: 1000px;
  padding: 50px;
  font-size: 50px;
  font-family:Quicksand, sans-serif;
}

.video{
  position:relative;
  padding-top:20px;
  padding-left: 150px;
  padding-right: 150px;
  padding-bottom: 100px;
}

.description{
  padding-left: 150px;
  padding-right: 150px;
  padding-bottom:150px;
}

.info{
  font-size: 40px;
}

p{
  font-size: 20px;
}
</style>

