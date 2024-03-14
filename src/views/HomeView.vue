<template>
  <v-app id="home">
    <NavBar />
    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative" class="mt-16">
              <h1 class="text-grey">Hello,</h1>
              <h1 class="text-white">I'm Kevin Chen</h1>
              <span class="text-grey">Web Designer & Developer</span>
              <br />
              <v-btn dark class="text-yellow mt-8" variant="outlined">
                Contact me
              </v-btn>
            </div>
          </v-col>
          <v-col cols="2">
            <div
              style="
                position: absolute;
                z-index: 9999;
                bottom: 0;
                margin-left: auto;
                margin-right: auto;
                left: 0;
                right: 0;
                text-align: center;
              "
            >
              <v-icon>fas fa-angle-double-down</v-icon>
            </div>
          </v-col>
          <v-col cols="5">
            <div style="position: relative; z-index: 9999" class="mt-16">
              <v-img src="favicon.ico" contain max-height="300"></v-img>
            </div>
          </v-col>
        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="6">
              <div class="egg">
                <v-img src="favicon.ico" max-height="300"></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h5 class="mt-16">About Me</h5>
              <div style="width: 120px">
                <v-slider v-model="slider2" color="yellow"></v-slider>
              </div>
              <h4 class="mt-n4">I am a Creative Web Designer</h4>
              <h4>and Developer</h4>
              <p class="text-grey">
                Lorem, ipsum dolor sit amet consectetur adipisicing elit. Optio
                vero, cumque, at illo, officia a dicta dolore temporibus ipsa
                harum dolorum ducimus quam laboriosam? Quis dolor placeat
                obcaecati aperiam natus.
              </p>
              <br />
              <p class="text-grey">
                Lorem, ipsum dolor sit amet consectetur adipisicing elit. Optio
                vero, cumque, at illo, officia a dicta dolore temporibus ipsa
                harum dolorum ducimus quam laboriosam? Quis dolor placeat
                obcaecati aperiam natus.
              </p>
              <v-btn dark color="yellow" class="mt-4"> Download Resume </v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <div class="text-center mt-4">
        <h2>What we Do</h2>
        <div style="width: 120px; margin: 0 auto">
          <v-slider v-model="slider2" color="yellow"></v-slider>
        </div>
      </div>
      <v-col cols="12" class="padd" id="portfolio">
        <div class="first" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child">
                <v-btn
                  icon="fas fa-laptop"
                  color="#FBDF7E"
                  class="tet-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">Web Design</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem ipsum dolor sit amet consectetur <br />
                  adipisicing elit. Maxime odit tempora doloribus<br />
                  beatae est impedit nulla hic
                </p>
              </div>
              <div class="child">
                <v-btn
                  icon="fas fa-mobile-alt"
                  color="#FBDF7E"
                  class="tet-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">App Design</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem ipsum dolor sit amet consectetur <br />
                  adipisicing elit. Maxime odit tempora doloribus<br />
                  beatae est impedit nulla hic
                </p>
              </div>
              <div class="child">
                <v-btn
                  icon="fas fa-camera"
                  color="#FBDF7E"
                  class="tet-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">Photography</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem ipsum dolor sit amet consectetur <br />
                  adipisicing elit. Maxime odit tempora doloribus<br />
                  beatae est impedit nulla hic
                </p>
              </div>
            </v-col>
          </v-row>
          <v-divider></v-divider>
        </div>
      </v-col>
      <v-col cols="12" sm="12" id="services">
        <div class="d-flex justify-center mb-6">
          <v-btn color="#FBDF7E" class="mr-2">All</v-btn>
          <v-btn class="mr-2" variant="tonal">Web Design</v-btn>
          <v-btn class="mr-2" variant="tonal">Front Design</v-btn>
          <v-btn class="mr-2" variant="tonal">Photography</v-btn>
          <v-btn variant="tonal">Illustration</v-btn>
        </div>
      </v-col>
      <v-col cols="12" class="imgHover">
        <v-row class="fill-height" align="center" justify="center">
          <template v-for="(item, i) in items" :key="i">
            <v-col cols="12" md="4">
              <v-hover v-slot="{ isHovering, props }">
                <v-card
                  :elevation="isHovering ? 12 : 2"
                  :class="{ 'on-hover': isHovering }"
                  v-bind="props"
                >
                  <v-img :src="item.img" height="225px" cover></v-img>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
      </v-col>
      <v-col cols="12" sm="12">
        <div class="d-flex justify-center mb-6">
          <v-btn color="#FBDF7E" class="mt-4">Load More</v-btn>
        </div>
      </v-col>
      <v-col cols="12" id="page">
        <div class="pre">
          <v-row>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="favicon.ico" height="200px"></v-img>
                <v-card-title>We provide you the best</v-card-title>
                <v-card-subtitle>By Kevin Chen | 14 mar 2024</v-card-subtitle>
                <v-card-text>
                  Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                  Earum,
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="favicon.ico" height="200px"></v-img>
                <v-card-title>We provide you the best</v-card-title>
                <v-card-subtitle>By Kevin Chen | 14 mar 2024</v-card-subtitle>
                <v-card-text>
                  Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                  Earum,
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344px" height="350px">
                <v-img src="favicon.ico" height="200px"></v-img>
                <v-card-title>We provide you the best</v-card-title>
                <v-card-subtitle>By Kevin Chen | 14 mar 2024</v-card-subtitle>
                <v-card-text>
                  Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                  Earum,
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" id="blog">
        <div class="hire">
          <v-row>
            <v-col cols="12" sm="8">
              <h1 class="mt-9">Hire me for your awesome project</h1>
              <p class="text-grey">
                Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                Aliquid aspernatur perferendis enim fuga ut
              </p>
            </v-col>
            <v-col cols="12" sm="4">
              <v-btn color="#FBDF7E" class="mr-15">Hire Me</v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" sm="12" class="px-16" id="contact">
        <v-row>
          <v-col cols="12" sm="4">
            <div class="child">
              <h1>Contact info.</h1>
              <v-btn
                icon="fas fa-map-marker-alt"
                class="mt-10"
                variant="outlined"
              /><br />
              <span class="text-caption">Your Street SYO, Your Area Dream</span
              ><br />
              <v-btn
                icon="fas fa-phone-alt"
                class="mt-10"
                variant="outlined"
              /><br />
              <span class="text-caption">00235-6547</span><br />
              <span class="text-caption">00235-6547</span><br />
              <v-btn
                icon="fas fa-envelope"
                class="mt-10"
                variant="outlined"
              /><br />
              <span class="text-caption">asdfghjkl@gmail.com</span><br />
              <span class="text-caption">asdfghjkl@gmail.com</span><br />
            </div>
          </v-col>
          <v-col cols="12" sm="8">
            <h1 class="mt-8">Send your message</h1>
            <v-divider></v-divider>
            <span class="text-caption">
              Lorem ipsum, dolor sit amet consectetur adipisicing elit.
              Distinctio tempore earum sit, amet fugiat deleniti repudiandae
              dolor veniam officia odio soluta, fugit excepturi dolorum quos
              iste saepe exercitationem esse ipsa!
            </span>
            <v-row class="mt-10">
              <v-col cols="12" sm="6">
                <v-text-field
                  label="Name"
                  persistent-hint
                  variant="outlined"
                ></v-text-field>
              </v-col>
              <v-col cols="12" sm="6">
                <v-text-field
                  label="Phone No"
                  persistent-hint
                  variant="outlined"
                ></v-text-field>
              </v-col>
            </v-row>
            <v-textarea
              label="Message"
              persistent-hint
              variant="outlined"
            ></v-textarea>
            <v-btn color="#FBDF7E" class="mt-2">Submit Now</v-btn>
          </v-col>
        </v-row>
      </v-col>
    </v-container>
    <FooterView />
  </v-app>
</template>

<script>
import { defineComponent } from "vue";

// Components
import NavBar from "../components/NavBar.vue";
import FooterView from "./FooterView.vue";

export default defineComponent({
  name: "HomeView",
  setup() {
    return {
      slider2: 50,
      items: [
        {
          img: "favicon.ico",
        },
        {
          img: "favicon.ico",
        },
        {
          img: "favicon.ico",
        },
        {
          img: "favicon.ico",
        },
        {
          img: "favicon.ico",
        },
        {
          img: "favicon.ico",
        },
      ],
    };
  },

  components: {
    NavBar,
    FooterView,
  },
});
</script>

<style scoped>
.v-container {
  padding: 16px 0;
}
.head {
  position: relative;
  text-align: center;
  padding: 12px;
  margin-bottom: 6px;
  width: 100%;
  height: 400px;
  color: white;
}
.head::before {
  content: " ";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, 6deg);
}
.head::after {
  content: " ";
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, -6deg);
}
.egg {
  display: block;
  margin-left: 100px;
  margin-top: 50px;
  width: 356px;
  height: 300px;
  background: #fbdf7e;
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
}
.first {
  width: 100%;
  height: 280px;
  text-align: center;
  padding: 2rem 2rem;
}
.child {
  display: inline-block;
  padding: 2rem 1rem;
  text-align: center;
  margin-right: 8px;
}
.imgHover {
  padding: 0 200px;
}
.pre {
  width: 100%;
  height: 380px;
  text-align: center;
  padding: 0 200px;
  background: #f5f5f5;
}
.hire {
  width: 100%;
  height: 200px;
  padding: 0 200px;
  background: #e9e9e9;
  margin-top: -24px;
}
</style>
