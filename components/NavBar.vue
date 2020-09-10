<template>
  <div class="row navbar-row">
    <nav class="col-md-12 navbar navbar-expand-lg navbar-light bg-white" style="padding: .6rem 2.5rem 0.6rem 2.5rem">
      <a class="nav-link" href="/landing" style="color: #53565A"><img style="max-width:80px" src="../static/images/well.png"></a>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ml-auto" >
          <li>
            <nuxt-link to="" class="nav-link">English</nuxt-link>
          </li>
          <li>
            
            <nuxt-link to="" class="nav-link">SignIn</nuxt-link>
          </li>
        </ul>  
        <!-- <ul class="navbar-nav ml-auto" >
          <li>
            <a href="/cn" class="nav-link">
              <locale-switcher :locales="['en', 'cn']" :show-full="true" ></locale-switcher>
            </a>
          </li>
          <li>
            <div class="dropdown" v-if="Object.values($root.globalUserInfo).length > 0" style="margin-top:5px">
              <a class="nav-link" id="dLabel" role="button" data-toggle="dropdown" data-target="#">{{$root.globalUserInfo.name}}<span class="lnr lnr-chevron-down mg-x-5 tx-10"></span></a>
              <ul class="dropdown-menu multi-level" role="menu" aria-labelledby="dropdownMenu">
                <li><a href="https://account.wellcertified.com/dashboard/project/v2" target="_blank"><i class="lnr lnr-apartment"></i> Dashboard</a></li>
                <li @click="signOut"><a href=""><i class="lnr lnr-power-switch"></i> {{ $t('signout') }}</a></li>
              </ul>
            </div>
            <a class="btn btn-info" href="/user/login" style="color: #fff;" v-else>{{ $t('signin') }}</a>
          </li>
        </ul> -->
      </div>
    </nav>
  </div>
</template>