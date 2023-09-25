<script setup>
import{ ref } from "vue";

  const CoffeeList = ref([
    { id: 1, name: 'TeaCoff', img: "https://d1e00ek4ebabms.cloudfront.net/production/40075a8a-5e87-45fe-a24d-cc2e6d7738b6.jpg" },
    { id: 2, name: 'Coffee Guys', img: "https://okcredit-blog-images-prod.storage.googleapis.com/2021/05/Coffee---Tea-Shop1--1-.jpg" },
    { id: 3, name: 'Elegrant Tea', img: "https://static.wixstatic.com/media/d78afb_0a71705bbb6943269ad3d6b8e68e2959~mv2.jpg/v1/fill/w_640,h_294,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/d78afb_0a71705bbb6943269ad3d6b8e68e2959~mv2.jpg" },
    { id: 4, name: 'Coffee Lab', img: "https://www.visitmesa.com/imager/s3_us-west-1_amazonaws_com/mesa-2019/images/Jarrods-Coffee-wide-view-3_6779f590680632ee6ed1060f38937405.jpg" },
    { id: 5, name: 'Two Tea', img: "https://rccl-h.assetsadobe.com/is/image/content/dam/royal/data/ship/spectrum/assets/renders/spectrum-of-the-seas-coffee-and-tea-shop.jpg?$750x420$" },
    { id: 6, name: 'Coffero', img: "https://mir-s3-cdn-cf.behance.net/project_modules/max_1200/e3539a49733633.58bd884b167cc.jpg" }
  ]);

</script>
<template>
    <!-- Coffee Products -->
    <div class="bg-body-tertiary me-md-3 pt-3 px-3 pt-md-5 px-md-5 text-center overflow-hidden"
      v-for="(coffee, index) in CoffeeList"
      :key="index"
    >
      <div class="my-3 p-3">
        <h2 class="display-5">{{ coffee.name }}</h2>
        <p class="lead">Sample Text {{ index+1 }}</p>
      </div>
      <div
        class="bg-dark shadow-sm mx-auto"
        style="width: 45%; height: 320px; margin-top: -20px; border-radius: 21px 21px 0 0;"
      >
        <img :src="coffee.img" width="450" height="300" style="margin-top: 10px;" />
      </div>
      <div class="d-flex gap-2 justify-content-center py-5">
        <RouterLink :to="{name:'coffee', params: {id: coffee.id }}" class="button" type="button">
          Coffee Detail {{ index+1 }} &nbsp;
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="18"
            height="18"
            fill="currentColor"
            class="bi bi-arrow-right"
            viewBox="0 1 16 16"
          >
            <path
              fill-rule="evenodd"
              d="M1 8a.5.5 0 0 1 .5-.5h11.793l-3.147-3.146a.5.5 0 0 1 .708-.708l4 4a.5.5 0 0 1 0 .708l-4 4a.5.5 0 0 1-.708-.708L13.293 8.5H1.5A.5.5 0 0 1 1 8z"
            />
          </svg>
        </RouterLink>
      </div>
    </div>
  </template>
  


<style>
.button {
 --color: #003c58;
 padding: 0.8em 1.7em;
 background-color: transparent;
 border-radius: .3em;
 position: relative;
 overflow: hidden;
 cursor: pointer;
 transition: .5s;
 font-weight: 400;
 font-size: 17px;
 border: 1px solid;
 font-family: inherit;
 text-transform: uppercase;
 color: var(--color);
 z-index: 1;
}

.button::before, .button::after {
 content: '';
 display: block;
 width: 50px;
 height: 50px;
 transform: translate(-50%, -50%);
 position: absolute;
 border-radius: 50%;
 z-index: -1;
 background-color: var(--color);
 transition: 1s ease;
}

.button::before {
 top: -1em;
 left: -1em;
}

.button::after {
 left: calc(100% + 1em);
 top: calc(100% + 1em);
}

.button:hover::before, .button:hover::after {
 height: 410px;
 width: 410px;
}

.button:hover {
 color: rgb(255, 255, 255);
}

.button:active {
 filter: brightness(.8);
}

.container {
  max-width: 960px;
}

.icon-link > .bi {
  width: .75em;
  height: .75em;
}


.site-header {
  background-color: rgba(0, 0, 0, .85);
  -webkit-backdrop-filter: saturate(180%) blur(20px);
  backdrop-filter: saturate(180%) blur(20px);
}
.site-header a {
  color: #643400;
  transition: color .15s ease-in-out;
}
.site-header a:hover {
  color: #643400;
  text-decoration: none;
}


.product-device {
  position: absolute;
  right: 0;
  bottom: -5%;
  width: 300px;
  height: 740px;
  background-color: #003c58;
  border-radius: 21px;

}

.product-device-2 {
  left: 0;
  background-color: #003c58;
}


.flex-equal > * {
  flex: 1;
}
@media (min-width: 768px) {
  .flex-md-equal > * {
    flex: 1;
  }
}

</style>