<template>
  <div id="sidebar">
    <b-container fluid>
      <b-row>
        <b-col>
          <NavBar />
          <button id="switch"  @click="toggleTheme">Switch</button>
        </b-col>
      </b-row>
    </b-container>

    <div class="br-sideleft bg-white overflow-y-scroll">
      <div class="br-sideleft-menu mg-t-10">
        <a class="br-menu-link" href="https://www.wellcertified.com">
          <div class="br-menu-item">
            <span class="menu-item-label">Back to website</span>
          </div>
        </a>
        <nuxt-link to="/landing/overview" class="br-menu-link">
          <div class="br-menu-item">
            <span class="menu-item-label">Overview</span>
          </div>
        </nuxt-link>
        <nuxt-link to="/landing/standard" class="br-menu-link">
          <div class="br-menu-item">
            <span class="menu-item-label">Standard</span>
          </div>
        </nuxt-link>
      </div>
    </div>
    <div class="br-mainpanel">
      <h1>Main Panel</h1>
    </div>
  </div>
</template>
<script>
import NavBar from '../components/NavBar'

export default {
  components: {
    NavBar
  }
  
}
</script>
<style scoped>
  .br-sideleft {
    position: absolute;
    top: 55px;
    left: 0px;
    bottom: 0;
    z-index: 2 !important;
    width: 230px;
    background-color: #333;
    padding-left: 0px;
    padding-right: 0px;
    transition: all 0.2s ease-in-out;
    border-radius:0;
  }
  .br-mainpanel{
    position:absolute;
    top: 55px;
    left:230px;
    z-index: 2;

  }
  .bg-white{
    background-color: #fff;
  }

  .br-menu-item{
    display: flex;
  }

</style>