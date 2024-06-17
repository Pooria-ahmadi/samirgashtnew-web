<template>
  <div>
    <div class="box is-hidden-mobile">
      <div class="columns">
        <div class="column is-half py-0">
          <div class="navbar-start is-hidden-mobile ">
            <a href="/">
              <img src="/logo/logo.jpg" class="logo"/>
            </a>
            <a class="navbar-item mr-6" href="#anali-card">
              آنالی کارت
            </a>
            <a class="navbar-item" href="#iran-card">
             ایران کارت
            </a>
            <a class="navbar-item" href="#mashhad-card">
             مشهد کارت
            </a>
          </div>

        </div>

        <div class="column is-half py-0">
          <div class="navbar-end is-hidden-mobile">

            <a href="tel:09100036700" class="button is-info is-rounded ml-6 has-text-weight-bold" width="20%">
              <img src="/opction/icons8-support-64.png">
              <p class="pr-4">09100036700</p>
            </a>
            <NuxtLink to="/login" class="button is-success is-hovered has-text-weight-bold">ثبت نام | ورود</NuxtLink>

          </div>
        </div>
      </div>
    </div>
  </div>
</template>