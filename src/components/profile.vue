<template> 
<div id="profilee">
    

    <div id="infobox"></div>
        <div id="infa"> 
            <h1 id="name">Lasma Strazdina</h1> <br>
            <h1 id="student">Multimedia design student</h1>
            <h2 class="col">E-mail <br></h2> <h3> lasmastraz@gmail.com <br></h3>
            <h2 class="col">Phone <br></h2> <h3>+371 24557737</h3>
            <h2 class="col">CV <br></h2> 

            <!-- Start of botton -->
            <div class="text-xs-center">
            <v-dialog
            v-model="dialog"
            width="500"
            >
            <template v-slot:activator="{ on }">
            <v-btn
            dark
            v-on="on"
            >
            Open CV
            </v-btn>
            </template>
            <v-card>
           <div id="cv"></div>
            </v-card>
             </v-dialog>
            </div>
             <!-- end of button -->
            
    </div>

    
</div>
</template>



<script>
export default {
    data () {
      return {
        dialog: false
      }
    }
  }
</script>



<style scoped>
   
    .v-card.v-sheet.theme--light {
        margin-top: -20px;
        height: 680px;
    }
    .v-btn__content {
       font-weight: lighter;
    }
    .v-btn.theme--dark {
        height: 15px;
        position: absolute;
        left: 0;
    }
    #cv {
        height: 680px;
        width: 500px;
        background-image: url("../assets/digital-cv.png");
        background-size: cover;
    }
    #name {
        color: white;
        font-family: 'Heebo', sans-serif;
        font-size: 23px;
        font-weight: 100;
        margin: 8px 0 0 8px;

    }
    #student {
        color: white;
        font-family: 'Heebo', sans-serif;
        font-size: 15px;
        font-weight: 100;
        margin: -20px 0 17px 8px;
    }
    h2 {
        color: gold;
        font-family: 'Heebo', sans-serif;
        font-size: 12px;
        font-weight: 100;
        margin-left: 8px
    }
    h3 {
        color: white;
        font-family: 'Heebo', sans-serif;
        font-size: 12px;
        font-weight: 100;
        margin: 1px 0 7px 8px;
    }
    #infobox {
        background-image: url("../assets/photoo.jpg");
        background-size: cover;
        width: 150px;
        height: 180px;
        position: absolute;
        top: 3%;
        left: 1%;
        display: flex;
        justify-content: center
        
    }
   
    #infa {
        background-color: #00000099;
        background: linear-gradient(124deg, rgba(0,0,0,1) 7%, rgba(0,0,0,0.9026961126247374) 15%, rgba(0,0,0,0.6870098381149334) 42%, rgba(0,0,0,0) 96%);
        width: 280px;
        height: 180px;
        position: absolute;
        top: 3%;
        left: 11%; 
    }
    #profilee {
        width: 465px;
        height: 210px;
        align-items: center;
        
    }

</style>
