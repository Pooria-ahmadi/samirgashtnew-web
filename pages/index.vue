<template>
  <div>
    <div class="slideshow-container m-auto">

<div v-for="(slide, index) in slides" :key="index" class="mySlides" v-show="index === currentSlide">
  <img :src="slide.image" alt="سمیرگشت " class="width-shadow-slider">
  <div class="Caption-text has-text-white has-text-weight-bold is-size-5 p-5 has-text-centered">{{ slide.caption }}</div>
</div>
<a class="next has-text-white has-text-weight-bold is-size-6" @click="prevSlide">&#10094;</a>
<a class="prev has-text-white has-text-weight-bold is-size-6" @click="nextSlide">&#10095;</a>
</div>

<div class="has-text-centered mt-4">
<span v-for="(dot, index) in slides" :key="index" class="dot" :class="{ 'active': index === currentSlide }" @click="changeSlide(index)"></span> 
</div>

    <div class="columns is-centered is-vcentered my-6 mx-6 has-background-success-light">
      <div class="column">
        <p class="has-text-weight-bold">سفر کارت چیست؟</p>
        <p class="mt-4 line-height-description">
          سفر کارت یک بسته سفر که با خرید آن می توان سفر را در خانواده برای بالا بردن سطح کیفیت زندگی با توجه
          به مشکلات روزمره بالا برد ، این کارت ها هم از لحاظ هزینه و هم از لحاظ کیفیت می تواند نظر استفاده
          کنندگان را تامین کند ،شایان ذکر است با خرید این کارت تورم را در طول استفاده به صفر رسانده و این
          مشخصه یکی از بارزترین مزایای این کارت ها می باشد
        </p>
        <div class="has-text-centered mt-6">
          <button class="button is-light has-background-success has-text-weight-semibold has-text-white"> ثبت
            درخواست</button>
        </div>

      </div>
      <div class="column has-text-centered">
        <img src="safarcards.jpg" alt="" class="border-all-image">
      </div>
    </div>
    <div class="columns is-centered is-vcentered mt-6 mx-6">
      <div class="column has-text-centered">
        <img src="/aboutus/support-agency.jpg" alt="" class="border-all-image">
      </div>
      <div class="column">
        <p class="has-text-weight-bold">آژانس ما همراه شما خواهد بود، در هر زمان....</p>
        <p class="mt-4 line-height-description">
          در اینجا ، هر سفر یک داستان خواندنی است . از شروع تا پایان ما به همراه شما هستیم تا مطمئن شویم که هر
          لحظه ،هر مکان و هر تجربه به بهترین شکل ممکن برای شما ارائه شود
          هماهنگی دقیق با هتل ها ، اقامتگاه های با کیفیت و طراحی تور های فراوان همگی جزئیاتی از سفرهایی هستند
          که
          ما طرح ریزی میکنیم
          آماده ایم تا همراه شما باشیم در هر قدم از سفرتان و ما به شما این امکان را میدهیم که زیبایی های جهان
          را
          لمس کنید
          با انتخاب آژانس گردشگری ما ، به دنیایی از ماجراجویی و کاوش خواهید رفت که هر زمان لبخند را برای شما
          به
          ارمغان می آورد

        </p>
      </div>
    </div>
    <div class="columns is-justify-content-center mt-4 mx-0" id="anali-card">
      <div class="column is-one-fifth">
        <p class=" has-text-weight-semibold is-size-2  has-text-centered">
          ANALI CARD
        </p>
      </div>
    </div>
    <div class="columns is-justify-content-center mt-4 mx-0">
      <div class=" column is-one-quarter mx-6">
        <div class="card">
          <div class="card-image">
            <figure class="image is-4by3">
              <img src="las-principales2.jpg" alt="Placeholder image">
            </figure>
          </div>
          <div class="card-content has-text-centered">
            <p class="has-text-weight-semibold is-size-5" style="color: orange;">
              کارت نارنجی
            </p>
            <p class="has-text-weight-semibold mt-3" style="color: orange;">
              دو سفره آپارتمان
            </p>
            <p class="mt-3">
              دو شب و سه روز اقامت در رامسر برای 4 نفر
            </p>
            <NuxtLink to="/login" class="button is-link is-rounded mt-6 has-text-weight-semibold">خرید</NuxtLink>
          </div>
        </div>
      </div>
      <div class=" column is-one-quarter mx-6">
        <div class="card">
          <div class="card-image">
            <figure class="image is-4by3">
              <img src="las-principales3.jpg" alt="Placeholder image">
            </figure>
          </div>
          <div class="card-content has-text-centered">
            <p class="has-text-weight-semibold has-text-success-dark is-size-5">
            کارت سبز
            </p>
            <p class="has-text-weight-semibold has-text-success-dark mt-3">
              تک سفره آپارتمان
            </p>
            <p class="mt-3">
              دو شب و سه روز اقامت در رامسر برای 4 نفر
            </p>
            <NuxtLink to="/login" class="button is-link is-rounded mt-6 has-text-weight-semibold">خرید</NuxtLink>
          </div>
        </div>
      </div>
      <div class=" column is-one-quarter mx-6">
        <div class="card">
          <div class="card-image">
            <figure class="image is-4by3">
              <img src="las-principales-gold.jpg" alt="Placeholder image">
            </figure>
          </div>
          <div class="card-content has-text-centered">
            <p class="has-text-weight-semibold has-text-warning-dark is-size-5">
              کارت طلایی
            </p>
            <p class="has-text-weight-semibold has-text-warning-dark mt-3">
              دو سفره آپارتمان
            </p>
            <p class="mt-3">
              سه شب و چهار روز اقامت در رامسر برای 4 نفر
            </p>
            <NuxtLink to="/login" class="button is-link is-rounded mt-6 has-text-weight-semibold">خرید</NuxtLink>
          </div>
        </div>
      </div>
    </div>
    <div class="columns is-justify-content-center mt-4 mx-0" id="iran-card">
      <div class="column is-one-fifth ">
        <p class=" has-text-weight-semibold is-size-2  has-text-centered">
          IRAN CARD
        </p>
      </div>
    </div>
    <div class="columns is-justify-content-center mt-4 mx-0">
      <div class=" column is-one-quarter mx-6">
        <div class="card">
          <div class="card-image">
            <figure class="image is-4by3">
              <img src="las-principales2.jpg" alt="Placeholder image">
            </figure>
          </div>
          <div class="card-content has-text-centered">
            <p class="has-text-weight-semibold is-size-5" style="color: orange;">
              کارت نارنجی
            </p>
            <p class="has-text-weight-semibold mt-3" style="color: orange;">
              3 ستاره و هتل آپارتمان
            </p>
            <p class="mt-3">
              دو شب و سه روز اقامت در رامسر برای 4 نفر
            </p>
            <p class="mt-3">
              دو شب و سه روز اقامت در مشهد برای 4 نفر
            </p>
            <p class="mt-3">
              دو شب و سه روز اقامت در کیش برای 4 نفر
            </p>
            <NuxtLink to="/login" class="button is-link is-rounded mt-6 has-text-weight-semibold">خرید</NuxtLink>
          </div>
        </div>
      </div>
      <div class=" column is-one-quarter mx-6">
        <div class="card">
          <div class="card-image">
            <figure class="image is-4by3">
              <img src="las-principales3.jpg" alt="Placeholder image">
            </figure>
          </div>
          <div class="card-content has-text-centered">
            <p class="has-text-weight-semibold has-text-success-dark is-size-5">
            کارت سبز
            </p>
            <p class="has-text-weight-semibold has-text-success-dark mt-3">
              3 ستاره و هتل آپارتمان
            </p>
            <p class="mt-3">
              دو شب و سه روز اقامت در رامسر برای 4 نفر
            </p>
            <p class="mt-3">
              دو شب و سه روز اقامت در مشهد برای 4 نفر
            </p>
            <NuxtLink to="/login" class="button is-link is-rounded mt-6 has-text-weight-semibold">خرید</NuxtLink>
          </div>
        </div>
      </div>
      <div class=" column is-one-quarter mx-6">
        <div class="card">
          <div class="card-image">
            <figure class="image is-4by3">
              <img src="las-principales4.jpg" alt="Placeholder image">
            </figure>
          </div>
          <div class="card-content has-text-centered">
            <p class="has-text-weight-semibold has-text-link-dark is-size-5">
              کارت آبی
            </p>
            <p class="has-text-weight-semibold has-text-link-dark mt-3">
              3 ستاره و هتل آپارتمان
            </p>
            <p class="mt-3">
              دو شب و سه روز اقامت در رامسر برای 4 نفر
            </p>
            <p class="mt-3">
              دو شب و سه روز اقامت در کیش / قشم برای 4 نفر
            </p>
            <NuxtLink to="/login" class="button is-link is-rounded mt-6 has-text-weight-semibold">خرید</NuxtLink>
          </div>
        </div>
      </div>
    </div>
    <div class="columns is-justify-content-center mt-4 mx-0" id="mashhad-card">
      <div class="column ">
        <p class=" has-text-weight-semibold is-size-2  has-text-centered">
          MASHHAD CARD
        </p>
      </div>
    </div>
    <div class="columns is-justify-content-center mt-4 mx-0">
      <div class=" column is-one-quarter mx-6">
        <div class="card">
          <div class="card-image">
            <figure class="image is-4by3">
              <img src="las-principales4.jpg" alt="Placeholder image">
            </figure>
          </div>
          <div class="card-content has-text-centered">
            <p class="has-text-weight-semibold is-size-5 has-text-link-dark">
              کارت آبی
            </p>
            <p class="has-text-weight-semibold mt-3 has-text-link-dark">
              4 ستاره
            </p>
            <p class="mt-3">
              اقامت با صبحانه دو شب و سه روز برای 4 نفر
            </p>
            <NuxtLink to="/login" class="button is-link is-rounded mt-6 has-text-weight-semibold">خرید</NuxtLink>
          </div>
        </div>
      </div>
      <div class=" column is-one-quarter mx-6">
        <div class="card">
          <div class="card-image">
            <figure class="image is-4by3">
              <img src="las-principales3.jpg" alt="Placeholder image">
            </figure>
          </div>
          <div class="card-content has-text-centered">
            <p class="has-text-weight-semibold has-text-success-dark is-size-5">
            کارت سبز
            </p>
            <p class="has-text-weight-semibold has-text-success-dark mt-3">
              3 ستاره و هتل آپارتمان
            </p>
            <p class="mt-3">
              اقامت فولبرد دو شب و سه روز برای 4 نفر
            </p>
            <NuxtLink to="/login" class="button is-link is-rounded mt-6 has-text-weight-semibold">خرید</NuxtLink>
          </div>
        </div>
      </div>
      <div class=" column is-one-quarter mx-6">
        <div class="card">
          <div class="card-image">
            <figure class="image is-4by3">
              <img src="las-principales-gold.jpg" alt="Placeholder image">
            </figure>
          </div>
          <div class="card-content has-text-centered">
            <p class="has-text-weight-semibold has-text-warning-dark is-size-5">
              کارت طلایی
            </p>
            <p class="has-text-weight-semibold has-text-warning-dark mt-3">
              5 ستاره
            </p>
            <p class="mt-3">
              اقامت با صبحانه دو شب و سه روز برای 4 نفر
            </p>
            <NuxtLink to="/login" class="button is-link is-rounded mt-6 has-text-weight-semibold">خرید</NuxtLink>
          </div>
        </div>
      </div>
    </div>
    <div class="columns is-justify-content-center mt-6 mx-5">
      <div class="box column is-three-quarters has-background-grey-lighter">
        <p class="has-text-weight-bold mr-4 my-4">
          نیاز به راهنمایی بیشتر دارید؟
        </p>
        <p class="has-text-weight-semibold">
          برای آگاهی از شرایط ویژه و سفارش سفرکارت سمیر گشت، فرم زیر را تکمیل کنید یا درخواست خود را به آدرس ایمیل
          SHARAREHABDI31@YAHOO.COM بفرستید.
        </p>
        <div class="columns mt-6">
          <div class="column is-one-quarter">
            <input class="input" type="text" placeholder="نام و نام خانوادگی*">
          </div>
          <div class="column is-one-quarter">
            <input class="input" type="text" placeholder="شماره همراه*">
          </div>
          <div class="column is-one-quarter">
            <input class="input" type="text" placeholder="آدرس ایمیل*">
          </div>
          <div class="column is-one-quarter">
            <input class="input" type="text" placeholder="نام سازمان*">
          </div>
        </div>
        <div class="columns">
          <div class="column is-one-quarter">
            <input class="input" type="text" placeholder="مبلغ کل درخواستی*">
          </div>
        </div>
        <div class="columns is-vcentered">
          <div class="column is-three-fifths">
            <input class="input height-input-form-safarcart" type="text" placeholder="توضیحات *">
          </div>
          <div class="column has-text-centered">
            <button class="button is-link">
              <p class="has-text-weight-bold">
                ثبت درخواست
              </p>
            </button>
          </div>
        </div>
      </div>
    </div>
    <div class="background-fixed">
      <div class="columns is-centered is-vcentered mx-6 mt-65 white-color-text">
        <div class="column">
          <p class="has-text-weight-bold">سفر کارت چیست؟</p>
          <p class="mt-4 line-height-description">سفر سفر کارت یک بسته سفره که با خرید آن می توان سفر را در خانواده برای بالا بردن سطح کیفیت زندگی با توجه به مشکلات روزمره بالا برد ، این کارت ها هم از لحاظ هزینه و هم از لحاظ کیفیت می تواند نظر استفاده کنندگان را تامین کند</p>
          <div class="has-text-centered mt-6">
            <button class="button is-light">
              <NuxtLink class="has-text-grey-dark" to="/services-services">ادامه مطلب...</NuxtLink>
            </button>
          </div>

        </div>
        <div class="column has-text-centered">
          <img src="/index/safar-card.jpg" alt="" class="border-all-image">
        </div>
      </div>
      <div class="columns is-centered is-vcentered  mx-6 mt-5 white-color-text">
        <div class="column has-text-centered">
          <img src="/index/laptab.jpg" alt="" class="border-all-image">
        </div>
        <div class="column">
          <p class="has-text-weight-bold"> چرا باید سفر کارت بخرید : </p>
          <ul>
            <li class="mt-4 line-height-description">ما سفر رفتن رو برای شما راحت میکنیم. ما شمارو از تورم نجات میدیم.
            </li>
            <li class="mt-4 line-height-description">ما به شما حریم خصوصی سفر میدیم.</li>
            <li class="mt-4 line-height-description">ما به شما قدرت تصمیم گیری برای زمان و مکان سفر میدهیم. </li>
            <li class="mt-4 line-height-description">ما به شما زمان کنار خانواده بودن را هدیه میدهیم.</li>
            <li class="mt-4 line-height-description">ما برای شما خاطره به جا میگذاریم.</li>
            <li class="mt-4 line-height-description">ما شمارو از تورم نجات میدیم.</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="is-flex is-justify-content-center mt-65">
      <img src="question-mark.png" alt="">
      <p class="pt-2 mr-3 has-text-weight-bold">
        سوالات متداول
      </p>
    </div>
    <div class="columns is-centered mx-0 my-4" v-for="(item, index) in collapses">
      <a class="column is-two-thirds border-question-box">
        <div class="box has-background-grey-lighter">
          <div class="collapse-panel">
            <div class="collapse-header" @click="toggleCollapse(index)">
              <p class="is-size-6 has-text-weight-bold has-text-grey-dark">
                <span>
                  {{ item.titlecollaps }}
                </span>
                <img :src="item.isCollapsed ? '/opction/up-arrow.png' : '/opction/down-arrow.png'" alt="arrow-icon"
                  class="direction-img-left-question" />
              </p>
            </div>
            <div class="collapse-body mr-4 line-height-description"
              :class="{ 'collapse-transition': true, 'collapsed': item.isCollapsed, 'expanded': !item.isCollapsed }">
              <p>{{ item.subCollapse }}</p>
            </div>
          </div>
        </div>
      </a>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      collapses: [
        { isCollapsed: true, titlecollaps: "نرخ بلیط هواپیما برای نوزادان و کودکان زیر ۱۲ سال چگونه است؟", subCollapse: "نرخ بلیط کودکان و نوزادان به کلاس پرواز و کلاس نرخی بستگی دارد. به صورت کلی، قیمت بلیط مسافر کودک (2 الی 12 سال) معادل 50 الی 100 درصد بلیط بزرگسال، و قیمت بلیط مسافر نوزاد (تا دو سال) 10 درصد بلیط بزرگسال است." },
        { isCollapsed: true, titlecollaps: "آیا پس از خرید اینترنتی بلیط هواپیما امکان استرداد آن وجود دارد؟", subCollapse: "وقتی از سمیرگشت یعنی بهترین سایت خرید بلیط هواپیما ، بلیطتان را رزرو می‌کنید، خیالتان آسوده است که امکان استرداد وجه در صورت کنسل کردن بلیط وجود دارد. میزان جریمه را هم هنگام رزرو آنلاین بلیط هواپیما در قسمت قوانین استرداد بخوانید." },
        { isCollapsed: true, titlecollaps: "چند روز قبل از پرواز، بلیط هواپیما را بخریم؟", subCollapse: "امکان رزرو بلیط هواپیما از ماه‌ها قبل وجود دارد. اما گاهی اوقات قیمت بلیط هواپیما در روزهای نزدیک به پرواز ارزان‌تر می‌شود. بنابراین در صورتی که شرایطتان اجازه می‌دهد، رزرو آنلاین بلیط هواپیما را به روزهای نزدیک پرواز موکول کنید." },
        { isCollapsed: true, titlecollaps: "رزرو آنلاین بلیط هواپیما هزینه بیشتری از خرید حضوری دارد؟", subCollapse: "خیر؛ زمانی که از یک سایت معتبر خرید بلیط هواپیما، اقدام به خرید می‌کنید، نه تنها هزینه بیشتری پرداخت نمی‌کنید، حتی ممکن است تخفیف هم بگیرید." },
        { isCollapsed: true, titlecollaps: "آیا پس از خرید بلیط هواپیما، امکان تغییر نام یا نام خانوادگی وجود دارد؟", subCollapse: "در پرواز داخلی یا خارجی، امکان تغییر نام و نام خانوادگی در بلیط سیستمی وجود ندارد. اما در بلیط چارتر، برخی از چارترکننده‌ها این تغییر را می‌پذیرند." },
      ],
      currentSlide: 0,
    slides: [
      { image: '/poster-pages/slide1.jpg', caption: '' },
      { image: '/poster-pages/slide2.jpg', caption: '' },
    ]
    }
  },
  mounted() {
    this.showSlides();
  },
  methods: {
    toggleCollapse(index) {
      this.collapses[index].isCollapsed = !this.collapses[index].isCollapsed;
    },
    showSlides() {
      setInterval(() => {
        this.currentSlide = (this.currentSlide + 1) % this.slides.length;
      }, 5000);
    },
    changeSlide(index) {
      this.currentSlide = index;
    },
    prevSlide() {
      this.currentSlide = (this.currentSlide - 1 + this.slides.length) % this.slides.length;
    },
    nextSlide() {
      this.currentSlide = (this.currentSlide + 1) % this.slides.length;
    }
  },
}
</script>
