<template>
  <div class="home">
    <div id="loader-wrapper">
      <div id="quotes">
        <h1 class="font-weight-light text--darken-4 display-4 text-uppercase blue--text">
          We<label class="display-4 text-uppercase blue--text">Perform</label>
        </h1>
        <p class="display-2 blue-grey--text">Practice like you've never won.</p>
        <p class="display-2 blue-grey--text">Perform like you've never lost.</p>
      </div>
      <div id="loader"></div>
      <div class="loader-section section-left"></div>
      <div class="loader-section section-right"></div>
    </div>
    <div class="md-layout">
      <div class="md-layout-item md-size-66 mx-auto md-small-size-100">
        <v-carousel
                :per-page="1"
                loop
                :speed="1000"
                autoplay
                :autoplay-timeout="4000"
                :mouse-drag="true"
                navigationEnabled
                navigationNextLabel="<i class='material-icons'>keyboard_arrow_right</i>"
                navigationPrevLabel="<i class='material-icons'>keyboard_arrow_left</i>"
                style="cursor: pointer"
        >
          <md-card>
            <v-carousel-item
                    v-for="(item,i) in items"
                    :key="i"
                    :src="item.src"
                    :title="item.title"
            >
              <p class="headline" @click="search">{{ item.title }}</p>
            </v-carousel-item>
          </md-card>
        </v-carousel>
      </div>
    </div>
    <p></p>
    <v-toolbar-title class="text-uppercase">
      <h2 align="center">
        <span class="font-weight-light display-4 grey--text">We</span>
        <span class="display-4 black--text">Perform</span>
      </h2>
      <p></p>
      <v-layout>
        <v-flex xs4 sm12 sm8>
          <v-toolbar-title class="text-uppercase">
            <h2 align="center">
              <span class="blue-grey--text font-weight-bold display-2"><pre>Search</pre></span>
            </h2>
          </v-toolbar-title>
        </v-flex>
        <v-flex xs6 sm12 offset-sm1>
          <v-toolbar-title class="text-uppercase">
            <h2 align="center">
              <span class="blue-grey--text font-weight-bold display-2"><pre>Save</pre></span>
            </h2>
          </v-toolbar-title>
        </v-flex>
        <v-flex xs8 sm12 offset-sm1>
          <v-toolbar-title class="text-uppercase">
            <h2 align="center">
              <span class="blue-grey--text font-weight-bold display-2"><pre>Book</pre></span>
            </h2>
          </v-toolbar-title>

        </v-flex>
      </v-layout>
      <p></p>
    </v-toolbar-title>
    <h5 class="font-weight-light black--text">
      Designed to streamline the process of booking performers for events. Each performer has a profile describing their skill, expertise, and contact information, allowing patrons to search and book them with ease. This service saves the patrons time, effort, and money in search of their ideal performer, while also providing performers with a dedicated platform to promote themselves.
    </h5>
    <br>
    <v-divider color="grey"></v-divider>
    <v-divider color="grey"></v-divider>
    <p></p>
    <v-layout row>
      <h2 class="font-weight-light display-3 black--text">
        <pre class="change-font">Book a talent for your events</pre>
        <h4 class="title font-weight-light"><v-icon>check_circle</v-icon> <label class="font-weight-bold"> Festivals</label></h4><p></p>
        <h4 class="title font-weight-light"><v-icon>check_circle</v-icon> <label class="font-weight-bold"> Weddings</label></h4><p></p>
        <h4 class="title font-weight-light"><v-icon>check_circle</v-icon> <label class="font-weight-bold"> Stage shows</label></h4><p></p>
        <h4 class="title font-weight-light"><v-icon>check_circle</v-icon> <label class="font-weight-bold"> Birthday parties</label></h4><p></p>
        <h4 class="title font-weight-light"><v-icon>check_circle</v-icon> <label class="font-weight-bold"> Annual functions</label></h4><p></p>
        <h4 class="title font-weight-light">We’ll help you book the
          <label class="font-weight-bold red--text"> perfect talent </label> based on your needs!
        </h4>
      </h2>
      <v-spacer></v-spacer>
      <v-flex md6>
        <v-card>
          <v-img
                  src="assets/img/talents/concert.jpg"
                  height="300px"
          >
          </v-img>
        </v-card>
      </v-flex>
    </v-layout>
    <br>
    <v-layout row>
      <v-flex xs12>
        <v-divider color="grey"></v-divider>
        <v-divider color="grey"></v-divider>
      </v-flex>
    </v-layout>
    <p></p>
    <v-layout row>
      <v-flex sm12>
        <v-card max-width="700px">
          <v-img
                  src="assets/img/talents/dancer_perform.jpg"
                  height="300px"
          >
          </v-img>
        </v-card>
      </v-flex>
      <v-flex xs2 sm12 sm6 align-end>
        <h2 class="font-weight-light display-3 black--text">
          <pre>Filtered search options</pre>
          <v-flex xs2 sm12 sm6 align-end>
            <h4 class="title font-weight-bold"><v-icon>check_circle</v-icon> Genre</h4>
            <p></p>
            <h4 class="title font-weight-bold"><v-icon>check_circle</v-icon> Styles</h4>
            <p></p>
            <h4 class="title font-weight-bold"><v-icon>check_circle</v-icon> Location</h4>
            <p></p>
            <h4 class="title font-weight-bold"><v-icon>check_circle</v-icon> Experience</h4>
            <p></p>
            <h4 class="title font-weight-bold"><v-icon>check_circle</v-icon> Availability</h4>
            <p></p>
            <h4 class="title font-weight-light">Search for your <label class="font-weight-bold red--text"> ideal performer </label>
              based on your category of artistic composition.
            </h4>
          </v-flex>
        </h2>
      </v-flex>
    </v-layout>
    <br>
    <v-layout row>
      <v-flex xs12>
        <v-divider color="grey"></v-divider>
        <v-divider color="grey"></v-divider>
      </v-flex>
    </v-layout>
    <p></p>
    <v-layout>
      <h2 class="font-weight-light display-3 black--text">
        <pre>Platform promoting talent</pre>
        <h4 class="title font-weight-light"><v-icon>check_circle</v-icon> <label class="font-weight-bold"> Represent yourself the way you want to</label></h4><p></p>
        <h4 class="title font-weight-light"><v-icon>check_circle</v-icon> <label class="font-weight-bold"> Post your experience for recognition</label></h4><p></p>
        <h4 class="title font-weight-light"><v-icon>check_circle</v-icon> <label class="font-weight-bold"> Earn while engaging others</label></h4><p></p>
        <h4 class="title font-weight-light"><v-icon>check_circle</v-icon> <label class="font-weight-bold"> Build your own connections</label></h4><p></p>
        <h4 class="title font-weight-light"><v-icon>check_circle</v-icon> <label class="font-weight-bold"> Become a performer!</label></h4><p></p>
        <h4 class="title font-weight-light">The only platform giving chance to promote yourself,
          <label class="font-weight-light red--text">We</label>
          <label class="font-weight-bold red--text">Perform</label>.
        </h4>
      </h2>
      <v-spacer></v-spacer>
      <v-flex md6>
        <v-card>
          <v-img
                  src="assets/img/talents/singer_perform.jpg"
                  height="300px"
          >
          </v-img>
        </v-card>
      </v-flex>
    </v-layout>
    <p></p>
    <v-divider color="grey"></v-divider>
    <v-divider color="grey"></v-divider>
    <v-divider color="grey"></v-divider>
    <v-divider color="grey"></v-divider>
    <v-divider color="grey"></v-divider>
    <!--<p></p>-->
    <!--<v-layout>-->
    <!--<v-flex xs4 sm12 sm8>-->
    <!--<v-hover>-->
    <!--<v-toolbar-title class="text-uppercase">-->
    <!--<h2 align="center">-->
    <!--<PopupPerformer/>-->
    <!--</h2>-->
    <!--</v-toolbar-title>-->
    <!--</v-hover>-->
    <!--</v-flex>-->
    <!--</v-layout>-->
    <!--<p></p>-->
    <div class="footer">
      <div class="footer_content">
        <div>
          <ul>
            <li>
              <h3><a href="#">FEATURE</a></h3>
            </li>
            <li>
              <a href="#">Search</a>
            </li>
            <li>
              <a href="#">Save</a>
            </li>
            <li>
              <a href="#">Book</a>
            </li>
          </ul>
        </div>
        <div>
          <ul>
            <li>
              <h3><a href="/performers">PERFORMERS</a></h3>
            </li>
            <li>
              <a href="#">Dancer</a>
            </li>
            <li>
              <a href="#">Musician</a>
            </li>
            <li>
              <a href="#">Singer</a>
            </li>
            <li><p></p></li>
          </ul>
        </div>
        <div>
          <ul>
            <li>
              <h3><a href="#">EVENTS</a></h3>
            </li>
            <li>
              <a href="#">Metro Vancouver</a>
            </li>
            <li>
              <a href="#">Burnaby</a>
            </li>
            <li>
              <a href="#">Surrey</a>
            </li>
          </ul>
        </div>
        <div>
          <ul>
            <li>
              <h3><a href="#">CAREER</a></h3>
            </li>
            <li>
              <a href="#">Full Time</a>
            </li>
            <li>
              <a href="#">Part Time</a>
            </li>
          </ul>
        </div>
        <div>
          <ul>
            <li>
              <h3><a href="/about">ABOUT</a></h3>
            </li>
            <li>
              <a href="/about">About Us</a>
            </li>
            <li>
              <a href="/about">About WePerform</a>
            </li>
          </ul>
        </div>
        <div>
          <ul>
            <li>
              <h3><a href="#">FORUM</a></h3>
            </li>
            <li>
              <a href="#">Comment</a>
            </li>
            <li>
              <a href="#">Suggestion</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        items: [
          {
            src: '/assets/img/talents/dancer.jpg',
            title: "Dancer"
          },
          {
            src: '/assets/img/talents/musicians_stage.jpg',
            title: "Musician"
          },
          {
            src: '/assets/img/talents/singer_stage.jpg',
            title: "Singer"
          }
        ]
      }
    },
    methods: {
      search() {
        this.$router.replace('/performers')
      }
    }
  }
</script>

<style scoped>
  #loader-wrapper {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 1000;
  }
  #loader {
    display: block;
    position: relative;
    left: 50%;
    top: 25%;
    width: 300px;
    height: 300px;
    margin: -150px 0 0 -150px;
    border-radius: 50%;
    border: 3px solid transparent;
    border-top-color: #3498DB;
    -webkit-animation: spin 1.5s linear infinite; /* Chrome, Opera 15+, Safari 5+ */
    animation: spin 1.5s linear infinite; /* Chrome, Firefox 16+, IE 10+, Opera */
    z-index: 1001;
  }
  #quotes{
    color: white;
    font-size: 5vw;
    display: block;
    position: relative;
    left: 6%;
    top: 10%;
    z-index: 1001;
  }
  #quotes img{
    position: absolute;
    left: 25%;
    top:15%;
    width: 30%;
    z-index: -1;
  }
  #loader::before{
    content: "";
    position: absolute;
    top: 5px;
    left: 5px;
    right: 5px;
    bottom: 5px;
    border-radius: 50%;
    border: 3px solid transparent;
    border-top-color: #E74C3C;
    -webkit-animation: spin 3s linear infinite; /* Chrome, Opera 15+, Safari 5+ */
    animation: spin 3s linear infinite; /* Chrome, Firefox 16+, IE 10+, Opera */
  }
  #loader::after{
    content: "";
    position: absolute;
    top: 15px;
    left: 15px;
    right: 15px;
    bottom: 15px;
    border-radius: 50%;
    border: 3px solid transparent;
    border-top-color: #F9C927;
    -webkit-animation: spin 1.5s linear infinite; /* Chrome, Opera 15+, Safari 5+ */
    animation: spin 1.5s linear infinite; /* Chrome, Firefox 16+, IE 10+, Opera */
  }
  @-webkit-keyframes spin {
    0% {
      -webkit-transform: rotate(0deg);
      -ms-transform: rotate(0deg);
      transform: rotate(0deg);
    }
    100% {
      -webkit-transform: rotate(360deg);
      -ms-transform: rotate(360deg);
      transform: rotate(360deg);
    }
  }
  @keyframes spin {
    0% {
      -webkit-transform: rotate(0deg);
      -ms-transform: rotate(0deg);
      transform: rotate(0deg);
    }
    100% {
      -webkit-transform: rotate(360deg);
      -ms-transform: rotate(360deg);
      transform: rotate(360deg);
    }
  }
  #loader-wrapper .loader-section {
    position: fixed;
    top: 0;
    width: 51%;
    height: 100%;
    background: #262626;
    z-index: 1000;
  }
  #loader-wrapper .loader-section.section-left{
    left: 0;
  }
  #loader-wrapper .loader-section.section-right{
    right: 0;
  }
  .loaded #loader-wrapper .loader-section.section-left{
    -webkit-transform: translateX(-100%);
    -ms-transform: translateX(-100%);
    transform: translateX(-100%);
    -webkit-transition: all 0.7s 0.3s cubic-bezier(0.645, 0.045, 0.355, 1.000);  /* Android 2.1+, Chrome 1-25, iOS 3.2-6.1, Safari 3.2-6  */
    transition: all 0.7s 0.3s cubic-bezier(0.645, 0.045, 0.355, 1.000);  /* Chrome 26, Firefox 16+, iOS 7+, IE 10+, Opera, Safari 6.1+  */
  }
  .loaded #loader-wrapper .loader-section.section-right{
    -webkit-transform: translateX(100%);
    -ms-transform: translateX(100%);
    transform: translateX(100%);
    -webkit-transition: all 0.7s 0.3s cubic-bezier(0.645, 0.045, 0.355, 1.000);  /* Android 2.1+, Chrome 1-25, iOS 3.2-6.1, Safari 3.2-6  */
    transition: all 0.7s 0.3s cubic-bezier(0.645, 0.045, 0.355, 1.000);  /* Chrome 26, Firefox 16+, iOS 7+, IE 10+, Opera, Safari 6.1+  */
  }
  .loaded #loader{
    opacity: 0;
    -webkit-transition: all 0.3s ease-out;  /* Android 2.1+, Chrome 1-25, iOS 3.2-6.1, Safari 3.2-6  */
    transition: all 0.3s ease-out;  /* Chrome 26, Firefox 16+, iOS 7+, IE 10+, Opera, Safari 6.1+  */
  }
  .loaded #quotes{
    opacity: 0;
    -webkit-transition: all 0.7s ease-out;  /* Android 2.1+, Chrome 1-25, iOS 3.2-6.1, Safari 3.2-6  */
    transition: all 0.7s ease-out;  /* Chrome 26, Firefox 16+, iOS 7+, IE 10+, Opera, Safari 6.1+  */
  }
  .loaded #loader-wrapper {
    visibility: hidden;
    -webkit-transform: translateY(-100%);
    -ms-transform: translateY(-100%);
    transform: translateY(-100%);
    -webkit-transition: all 0.3s 1s ease-out; /* Android 2.1+, Chrome 1-25, iOS 3.2-6.1, Safari 3.2-6  */
    transition: all 0.3s 1s ease-out; /* Chrome 26, Firefox 16+, iOS 7+, IE 10+, Opera, Safari 6.1+  */
  }
  .headline{
    color: honeydew;
    padding: 410px 0;
    text-align: center;
  }
  h5{
    text-align: center;
    font-size: 18px;
    padding: 10px 0;
  }
  h1{
    padding: 10px 0;
    color:gray;
  }
  .footer{
    float: left;
    width: 100%;
    margin: 0 0 20px 0;
    margin-bottom: 0;
    background-color: black;
  }
  .footer ul{
    margin: 0 10% 0 0;
    font-size: 1vw;
    float: left;
  }
  .footer_content{
    width: 90%;
    float: left;
    margin: 0 10% 0 14%;
  }
  .footer_content div{
    float: left;
    width: 15%;
  }
  .footer_content ul{
    padding-left: 0;
    list-style: none;
  }
  .footer h3{
    font-size: 1vw;
    color: white;
  }
  .footer li a{
    color: gainsboro;
  }
  /*.change-font {*/
    /*font-family: "Trebuchet MS", Helvetica, sans-serif*/
  /*}*/
</style>