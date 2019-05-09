<template>
<div id="container">

<profile/>
<art/>


</div>
</template>

<script>
import art from "./components/art.vue"
import profile from "./components/profile.vue"

export default {
  name: 'App',
  
  components: {
    "art" :art,
    "profile" :profile,
  },

  data () {
    return {
    
    }
  }
}
</script>

<style>


  #container{
  background-image: url("./assets/dark-forest.jpg");
  height: 753px;
  width: 100%;
  background-size: cover;  
  }

@media screen and (max-width: 600px) {
#container {
  height: 1000px;
}
#infa {
 margin-left: 130px;
}
#infa[data-v-3d0b1749] {
  width: 355px;
}
#profilee {
  width: 600px;
  margin-right: -100px
}
#infobox {
  margin-left: 38px;
}
#big {
  position: relative;
  width: 700px;

}
.v-btn.theme--dark{
  bottom: 0%;
  right: 13%;
  z-index: 9999;
}
.v-tabs__bar.theme--dark.black, .v-tabs__wrapper {
  right: 0px;
  margin-top: 262px;
  margin-bottom: 60px;
  transform: rotate(0deg);
  z-index: 99999999;
}
#wan, #dei, #two, #tri, #fiv {
  transform: rotate(0deg);
}
#popdescr {
  width: 100px;
}
}


</style>
