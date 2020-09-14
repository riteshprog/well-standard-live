<template>
<div>
  <b-container fluid>
    <b-row>
      <b-col>
        <NavBar />
        <!-- <button id="switch"  @click="toggleTheme">Switch</button> -->
      </b-col>
    </b-row>
  </b-container>
  <b-container fluid>
    <div class="mg-15">
      <b-card class="card-w-shadow rounded">
        <b-card-body>
          <b-row>
            <b-col cols="12">
              <b-row>
                <b-col cols="10" offset="1">
                  <b-row>
                    <b-col md="6" style="padding: 5%;">
                      <h1 style="font-size: 3rem; margin-top: 1.5rem;">Our standards</h1>
                      <p class="tx-thin tx-18">We’re committed to improving global health by transforming the spaces where people spend their lives - and our suite of standards, geared toward both all types of buildings and communities, is designed to do exactly that. </p>
                    </b-col>
                    <b-col md="6" class="tx-center">
                      <img class="img-responsive" src="https://cdn.wellcertified.com/static/images/choice.png" style="max-height: 350px;" />
                    </b-col>
                  </b-row>
                </b-col>
              </b-row>
            </b-col>
            <b-col cols="12">
              <b-row style="background: #fff; padding-top: 100px">
                <b-col cols="10" offset="1">
                  <h1 class="text-center">Choose the best standard for your project</h1>
                </b-col>
                <b-col cols="10" offset="1">
                  <b-row>
                    <div class="col-12" style="padding: 1%">
                      <div class="row bg-gray-200" style="margin: 1%; border: 2px solid #429db5; border-radius: 6px;">
                        <div class="col-12 text-center mt-3">
                          <h3>WELL <span class="tx-thin">Health-Safety Rating</span></h3>
                          <p class="tx-14 tx-light">An evidence-based, third-party verified rating focused on facilities operations and management across multiple building types and spaces.</p>
                        </div>  
                        <div class="col-12 text-center mt-3 mb-3"> 
                          <nuxt-link class="btn btn-well-light" to="">Access Now</nuxt-link>
                          <a class="btn btn-well-light" :href="$root.latestVersions.v2hsr.en" v-if="isEnglish">Access Now</a>
                          <a class="btn btn-well-light" :href="$root.latestVersions.v2hsr.en" v-if="isChinese">Access Now</a>
                        </div>
                      </div>    
                    </div>
                  </b-row>
                  <b-row style="background: #fff">
                    <b-col md="4" cols="12" style="padding: 1%">
                      <div style="margin: 1%; border: 2px solid #D8D8D8; border-radius: 6px; padding: 4%">
                        <div class="text-centermt-3">
                              <img src="//a.storyblok.com/f/52232/300x113/3a5984cc5d/navlogos-v1-05.svg" class="Navigation__logo" style="width: 250px">
                              <p class="tx-14 tx-light">Launched in 2014, our original version of the WELL Building Standard helped the global community apply the principles of health to their spaces. </p>
                        </div>
                        <div class="text-center mt-3 mb-3">
                          <a class="btn btn-well-light" href="https://standard.wellcertified.com" target="_blank">Choose WELL v1</a>
                        </div>

                      </div>
                    </b-col>
                    <b-col md="4" cols="12" style="padding: 1%">
                      <div style="margin: 1%; border: 2px solid #429db5; border-radius: 6px; padding: 4%;">
                        <div class="text-center mt-3">
                          <img src="//a.storyblok.com/f/52232/x/f7bb234cba/wellv2.svg" class="Navigation__logo" style="width: 250px">
                          <p class="tx-14 tx-light">Updated in 2018, WELL v2 is the latest, most flexible and highest impact version of WELL, combining feedback from our users with the most current health data and research. </p>
                        </div>
                        <div class="text-center mt-3 mb-3">
                          <nuxt-link class="btn btn-well-light" to="/landing">Choose WELL v2</nuxt-link>
                          <a class="btn btn-well-light" :href="$root.latestVersions.v2pilot.en && $root.latestVersions.v2pilot.en" v-if="isEnglish">Choose WELL v2</a>
                          <a class="btn btn-well-light" :href="$root.latestVersions.v2pilot.cn && $root.latestVersions.v2pilot.cn" v-if="isChinese">Choose WELL v2</a>
                        </div>
                      </div>
                    </b-col>
                    <b-col md="4" cols="12" style="padding: 1%">
                      <div style="margin: 1%; border: 2px solid #D8D8D8; border-radius: 6px; padding: 4%">
                        <div class="text-center mt-3">
                          <img src="//a.storyblok.com/f/52232/x/cd7451c8d6/wellcommunityvertical.svg" class="Navigation__logo" style="width: 250px">
                          <p class="tx-14 tx-light">Expanded to the neighborhood scale, the WELL Community Standard applies the principles of WELL to a larger footprint.</p>
                        </div>
                        <div class="text-center mt-3 mb-3">
                          <nuxt-link class="btn btn-well-light" to="">Choose WELL Community</nuxt-link>
                          <a class="btn btn-well-light" :href="$root.latestVersions.community.en" v-if="isEnglish && $root.latestVersions.community.en">Choose WELL Community</a>
                          <a class="btn btn-well-light" :href="$root.latestVersions.community.cn" v-if="isChinese && $root.latestVersions.community.cn">Choose WELL Community</a>
                        </div>
                      </div>
                    </b-col>
                  </b-row>
                </b-col>
              </b-row>
            </b-col>
            <b-col cols="12">
              <b-row style="background: #fff; padding-top: 100px; padding-bottom:100px">
                <b-col cols="10" offset="1">
                  <h1 class="text-center">Our values</h1>
                </b-col>
                <b-col cols="10" offset="1">
                  <Footer />
                </b-col>
              </b-row>
            </b-col>
          </b-row>

        </b-card-body>
      </b-card>
    </div>
  </b-container>
</div>
</template>

<script>
import NavBar from '../components/NavBar'
import Footer from '../components/Footer'
export default {
  components: {
    NavBar,
    Footer
  },
  methods: {
    toggleTheme () {
      
      alert('change theme')
    }
  }
}
</script>

<style>
  h1 {
    font-family:museo-slab;
  }

.mg-15 {
    margin: 15px;
}
.tx-center {
    text-align: center;
}
.tx-18 {
    font-size: 18px;
}
.tx-thin {
    font-weight: 200;
}
.tx-14 {
    font-size: 14px;
}
.bg-gray-200 {
    background-color: #e9ecef;
}
.btn.btn-well-light {
  white-space: nowrap;
  display: inline-block;
  height: 40px;
  line-height: 40px;
  padding: 0 14px;
  -webkit-box-shadow: 0 4px 6px rgba(50,50,93,.11), 0 1px 3px rgba(0,0,0,.08);
  box-shadow: 0 4px 6px rgba(50,50,93,.11), 0 1px 3px rgba(0,0,0,.08);
  background: #429db5;
  border-radius: 3px;
  font-size: 14px;
  font-weight: 500;
  text-transform: uppercase;
  letter-spacing: .025em;
  color: #fff;
  text-decoration: none;
  -webkit-transition: all .15s ease;
  transition: all .15s ease;
}
</style>
