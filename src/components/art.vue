  <template>
    <div id="artbox">
        <div id="big">

          <!-- tabs start -->
          <div id="tabs">

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
          Description
        </v-btn>
      </template>

      <v-card>
        <v-card-title
          class="headline grey lighten-2"
          primary-title
        >
          Description
        </v-card-title>

        <v-card-text>
          <h3>Date:</h3> <p> 10/04/2018</p> <br>
          <h3>Size:</h3> <p>A5 (10,5cm x 7,4cm)</p> <br>
          <h3>Technique:</h3> <p>Lineart colored with pencils and gouache on paper</p>
        </v-card-text>

        <v-card-actions>
          
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
             <!-- end of button -->




            <v-tabs

              v-model="active"
              color="black"
              dark
              slider-color="yellow"
            >

              <v-tab class="tabwidth" id="wan" ripple></v-tab>
              <v-tab class="tabwidth" id="dei" ripple>  </v-tab>
              <v-tab class="tabwidth" id="two" ripple>  </v-tab>
              <v-tab class="tabwidth" id="tri" ripple>  </v-tab>
              <v-tab class="tabwidth" id="fiv" ripple> </v-tab>
            
              <v-tab-item>
              <v-card id="wanbig" flat>
                <div id="picframe1"></div>
              </v-card>
              </v-tab-item>
              
              <v-tab-item>
              <v-card id="wanbig" flat>
                <div id="picframeDei"></div>
              </v-card>
              </v-tab-item>

              <v-tab-item>
              <v-card id="wanbig" flat>
                <div id="picframe2"></div>
              </v-card>
              </v-tab-item>

              <v-tab-item>
              <v-card id="wanbig" flat>
                <div id="picframe3"></div>
              </v-card>
              </v-tab-item>

              <v-tab-item>
              <v-card id="wanbig" flat>
                <div id="picframefiv"></div>
              </v-card>
              </v-tab-item>

            </v-tabs>  
          </div>
              <!-- tabs end -->
        </div>



    </div> 
  </template>

  <script>
    export default {
  
      name: 'art',
    data (){
        return {
          dialog: false,
          active: null,
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'
        }
    },
     methods: {
        next () {
            const active = parseInt(this.active)
            this.active = (active < 2 ? active + 1 : 0)
        }
    }
    }
  </script>

  <style >
    .v-btn__content {
       font-weight: lighter;
    }
    .v-btn.theme--dark {
        height: 15px;
        position: absolute;
       right: 7%;}
    
    .v-tabs__bar.theme--dark.black, .v-tabs__wrapper {
      position: absolute !important;
      right: -261px;
      top:74px;
      transform: rotate(45deg);
      
    }
    .tabwidth {
      min-height: 70px;
      min-width:70px;
      
    
    }
    #big {
      position: relative;
      background-color:#000000;
      background: radial-gradient(circle, rgba(0,0,0,1) 33%, rgba(0,0,0,0.8018557764902836) 46%, rgba(0,0,0,0.569362779291404) 73%, rgba(0,0,0,0.33967090254070376) 84%, rgba(0,0,0,0) 98%);
      height: 670px;
      width: 900px;
      position: absolute;
      top:3%;  
      right: 9%;
      display: flex;
      justify-content: center
    }
 
    #wan {
      background-image: url("../assets/draw_cold.jpg");
      background-size: cover;
      transform: rotate(-90deg)
    }
    #two {
      background-image: url("../assets/draw_city.jpg");
      background-size: cover;
      transform: rotate(-90deg);
    }
    #tri {
      background-image: url("../assets/draw_night.jpg");
      background-size: cover;
      transform: rotate(-90deg);
    }
    #dei {
      background-image: url("../assets/draw_train.jpg");
      background-size: cover;
      transform: rotate(-90deg);
    }
    #fiv {
      background-image: url("../assets/draw_space.jpg");
      background-size: cover;
      transform: rotate(-90deg);
    }
    
    #picframe1 {
      height: 670px;
      width: 507px;
      background-image: url("../assets/draw_cold.jpg");
      background-size: cover;
      margin-top: -17px;
    }
    #picframe2 {
      height: 670px;
      width: 507px;
      background-image: url("../assets/draw_city.jpg");
      background-size: cover;
      margin-top: -17px;
    }
    #picframe3 {
      height: 670px;
      width: 507px;
      background-image: url("../assets/draw_night.jpg");
      background-size: cover;
      margin-top: -17px;
    }
    #picframeDei {
      height: 670px;
      width: 507px;
      background-image: url("../assets/draw_train.jpg");
      background-size: cover;
      margin-top: -17px;
    }
    #picframefiv {
      height: 670px;
      width: 507px;
      background-image: url("../assets/draw_space.jpg");
      background-size: cover;
      margin-top: -17px;
    }
  </style>