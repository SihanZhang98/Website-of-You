<template>
<b-container fluid>

<b-row class="header" >
  <b-col md="5">
    <b-img center rounded="circle" class="avatar"
      src="https://extendedevolutionarysynthesis.com/wp-content/uploads/2018/02/avatar-1577909_960_720.png"
      id="avatar-img"
    />
  </b-col>

  <b-col md="7" >
    <h2 class="intro">
      Hi!
      <br />I<span>'m Sihan Zhang</span>.
    </h2>

    <div class="info">
      A <b>Creative Technologist</b> and <b>Interactive Engineer</b> currently studying at <b>NYU ITP</b>.
      <br /> 
      Welcome to my space :)
    </div>
  </b-col>

  <br /> 
  <br /> 
  <br /> 
  <br /> 
</b-row>
  
  <b-row>
    <b-col cols="12" sm="12" md="6" lg="6"
        class="work"
        v-for="(work, i) of works"
        :key="i"
      >
        <NuxtLink :to="work.to">
        <img class="projectimg" :src="require(`../assets/${work.src}`)" :alt="work.title" />
        <h2 class="title">{{ work.title }}</h2>
      </NuxtLink>
      </b-col >
  </b-row>
</b-container>
</template>
<script>
  export default {
    data() {
      return {
        works: [
          { title: "Project 1", src: "img/img-1.jpg",to:"/project1" },
          { title: "Project 2", src: "img/img-2.jpg" ,to:"/project1"},
          { title: "Project 3", src: "img/img-3.jpg",to:"/project1" },
          { title: "Project 4", src: "img/img-4.jpg" ,to:"/project1"},
          { title: "Project 5", src: "img/img-5.jpg" ,to:"/project1"},
          { title: "Project 6", src: "img/img-6.jpg" ,to:"/project1"},
          { title: "Project 7", src: "img/img-7.jpg" ,to:"/project1"},
          { title: "Project 8", src: "img/img-8.jpg" ,to:"/project1"},
        ],
      };
    },
    methods: {
      onClick(work) {
        console.log("clicked: ", work);
      },
    },
  };
  </script>
  
<style scoped>
  body{ 
  font-family: Quicksand, sans-serif;
  text-align: center;
  background-image: url(~/assets/bg.svg);
  background-attachment: fixed;
  color: #000;
  }

  .header{
    padding-top: 80px;
    padding-bottom: 80px;
  }
  .intro {
  font-size: 55px;
  font-weight: bolder;
  text-align: left;

  /* margin-top: 20px; */

  /* color: #000; */
}

.avatar {
  background-color: rgb(46, 42, 42);
  width: 200px;
  height: 200px;
  cursor: pointer;
}

.title{
  font-size: 40px;
  position:absolute;
  top:50%;
  left:50%;
  transform:translate(-50%,-50%);
  color:#fff;
  opacity:0;
}
.projectimg{
  width:950px;

}
.work:hover h2{
  opacity:1;
  transition: opacity 0.3s;
}

.work:hover img{
  filter:brightness(0.25);
  transition: filter 0.3s;
}
</style>