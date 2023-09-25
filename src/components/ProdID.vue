<script setup>
import { ref } from "vue";
import { useRoute } from "vue-router";

const route = useRoute();
const id = parseInt(route.params.id);

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
 <div class="bg-body-tertiary me-md-3 pt-3 px-3 pt-md-5 px-md-5 text-center overflow-hidden">
    <div class="my-3 p-3">
    <RouterLink to="/" class="btn-back">Back</RouterLink>
    <h2 class="display-5">{{ CoffeeList[id - 1].name }}</h2>
      <p class="lead">Sample Text {{ id }}</p>
    </div>
    <div class="bg-dark shadow-sm mx-auto" style="width: 45%; height: 320px; margin-top: -20px; border-radius: 21px 21px 0 0;">
      <img :src="CoffeeList[id - 1].img" width="450" height="300" style="margin-top: 10px;" />
    </div> <br> <br>
   Lorem ipsum dolor sit amet consectetur adipisicing elit. Minima facere consectetur cum qui tempora? Odit similique ullam vitae eaque sint
    iste ipsa. Aspernatur quam quasi iusto possimus aliquid saepe, ut beatae deserunt nulla eos cupiditate adipisci aut dolores eaque iste 
    mollitia. Delectus enim quam esse corrupti ea? Eligendi magnam numquam quasi rerum saepe. Nisi autem quae veritatis magni fuga nihil at non 
    rerum, voluptates nulla officia cumque quis, impedit obcaecati sed dolor aliquam omnis? Magnam maxime aspernatur corrupti nulla fugit! 
    Accusantium voluptatum fugit harum ab! Impedit voluptate quod consectetur, eius pariatur ex at, placeat cupiditate exercitationem laborum,
    blanditiis ab recusandae?
 <br> <br> <br> </div> 
  </template>
  


<style>
.btn-back {
 margin-right: 90%;
 display: inline-block;
 padding: 0.5rem 1.8rem;
 font-size: 16px;
 font-weight: 700;
 color: rgb(72, 72, 72);
 border: 3px solid rgb(252, 70, 100);
 cursor: pointer;
 position: relative;
 background-color: transparent;
 text-decoration: none;
 overflow: hidden;
 z-index: 1;
 font-family: inherit;
 border-radius: 20px;
}

.btn-back::before {
 content: "";
 position: absolute;
 left: 0;
 top: 0;
 width: 100%;
 height: 100%;
 background-color: rgb(252, 70, 100);
 transform: translateX(-100%);
 transition: all .5s;
 z-index: -1;
}

.btn-back:hover::before {
 transform: translateX(0);
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