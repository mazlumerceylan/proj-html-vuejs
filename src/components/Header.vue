<template>
  <header>
    <div class="header-top d-flex align-items-center justify-content-between">
      <div class="lenguage-header d-flex align-items-center">
        <div class="btn-group">
          <button class="btn btn-secondary btn-sm dropdown-toggle language-button" type="button" data-bs-toggle="dropdown" aria-expanded="false">
            <span>{{ currentLanguage }}</span>
          </button>
          <ul class="dropdown-menu">
            <li v-for="(language, index) in languages" :key="index" @click="changeLanguage(language)">{{ language }}</li>
          </ul>
        </div>
      </div>
      <div class="header-top-right d-flex align-items-center justify-content-center">
        <button v-for="(buttonText, index) in headerButtons" :key="index" type="button" class="btn-style">{{ buttonText }}</button>
        <div class="header-top-icons">
          <i v-for="(icon, index) in socialIcons" :key="index" :class="`fab fa-${icon} icon-padding`"></i>
        </div>
      </div>
    </div>
    <div class="header-bottom d-flex align-items-center ml-2" style="height: 100px;">
      <div class="logo mx-1">
        <img src="../assets/img/MasterStudy_logo.svg" alt="LOGO">
      </div>
      <div class="dropdown-bottom">
        <i class="fa-solid fa-bars icon-main mx-2"></i>
        <button class="btn btn-secondary dropdown-toggle no-arrow icon-secondary" type="button" data-bs-toggle="dropdown" aria-expanded="false">CATEGORY</button>
        <ul class="dropdown-menu">
          <li v-for="(category, index) in categories" :key="index"><a class="dropdown-item" href="#">{{ category }}</a></li>
        </ul>
      </div>
      <nav class="navbar bg-body-tertiary">
        <div class="container-fluid">
          <form class="d-flex" role="search">
            <input class="form-control me-2" type="search" placeholder="Search courses" aria-label="Search">
            <button class="search icon-secondary">
              <i class="fa-solid fa-magnifying-glass"></i>
            </button>
          </form>
        </div>
      </nav>
      <div class="header-bottom-right d-flex align-items-center ml-5">
        <div class="r-side" v-for="(rightSideItem, index) in rightSideItems" :key="index">
          <i :class="`fa-solid ${rightSideItem.icon} icon-tertiary mx-2`"></i>
          <span>{{ rightSideItem.text }}</span>
        </div>
      </div>
      <div class="log-sign d-flex align-items-center ml-5">
        <div class="login">
          <i class="fa-regular fa-user icon-primary mx-2"></i>
          <span>Log In</span>
        </div>
        <div class="sign-up px-4">
          <button class="btn-rounded">Sign Up</button>
        </div>
        <div class="heart icon-primary mx-3">
          <i class="fa-regular fa-heart"></i>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import { mapState } from 'vuex'

export default {
  data() {
    return {
      currentLanguage: 'Italiano',
      rightSideItems: [
        {
          text: "Become an Instructor",
          icon: "fa-bullhorn"
        },
        {
          text: "For Enterprise",
          icon: "fa-suitcase"
        }
      ]
    }
  },
  computed: {
    ...mapState(['languages', 'headerButtons', 'socialIcons', 'categories'])
  },
  methods: {
    changeLanguage(language) {
      this.currentLanguage = language
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../scss/Header.scss';
</style>
