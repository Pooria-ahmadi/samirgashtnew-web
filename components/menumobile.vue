<template>
    <div>
        <nav class="navbar is-transparent is-hidden-desktop">
      <div class="navbar-brand is-flex-direction-row-reverse box py-0">
        <a class="is-hidden-desktop" href="/">
          <img src="/logo/logo.jpg" alt="logoagency" class="logo">
        </a>
        <div class="navbar-burger" :class="active ? 'is-active' : ''" @click="showMobilemenu">
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>
      <div class="navbar-menu pr-6 is-hidden-desktop" :class="active ? 'is-active' : ''">
        <ul>
          <li class="my-4">
            <a class="has-text-black has-text-weight-bold" href="#anali-card">
             آنالی کارت
            </a>
          </li>
          <li class="my-4">
            <a class="has-text-black has-text-weight-bold" href="#iran-card">
              ایران کارت
            </a>
          </li>
          <li class="my-4">
            <a class="has-text-black has-text-weight-bold" href="#mashhad-card">
              مشهد کارت
            </a>
          </li>
        </ul>
      </div>
    </nav>
    </div>
</template>
<script>
export default {
  data() {
    return {
      isActive: '',
      active: false,
    }
  },

  methods: {
    showMobilemenu() {
      //this.navbarBurgers
      console.log('is-active');
      this.active = !this.active;
    }
  }
}


</script>

