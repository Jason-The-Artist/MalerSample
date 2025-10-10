<style scoped>

.card{
  width: 100%;
  max-width: 450px;
  height: 310px;
  border: solid 1px;
  border-color: #e3e3e3;
}
.img-layout{
  height: 200px;
}

.product-img{
  object-fit: cover;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
}

.info-layout{
  width: 90%;
}

.black-tag{
  width: fit-content;
  border-radius: 100px;
  padding: 3px;
  padding-left: 6px;
  padding-right: 6px;
  background: #000000;
  color: white;
  font-size: 13px;
  font-weight: bold;
}

.overlay{
  background-color: rgba(0, 0, 0, 0);
  opacity: 0;
  transition: all 0.3s ease;
}
/*
.card:hover .overlay{
  background: rgba(0, 0, 0, 0.3);
  opacity: 1;
}

.card:hover{
  border-color: #6c98fb;
}
*/
</style>

<template>

  <div class="center-horizontal">
    <div class="card shadow round-corner">
      <div class="center-horizontal max-width img-layout relative">
        <img :src="'../../src/assets/projects/' + img" class="max-width max-height product-img cover">
        <div class="max-width max-height overlay absolute product-img center">
          <UIButton title="Details ansehen" sec style="background-color: #ffffff"/>
        </div>
      </div>
      <div style="height: 20px"></div>
      <div class="center-horizontal">
        <div class="info-layout">
          <div class="black-tag">Innenraumgestaltung</div>
          <div style="height: 10px"></div>
          <p class="reset-margin bold">{{title}}</p>
          <div style="height: 10px"></div>
          <p class="decent-color reset-margin">{{city}}</p>
        </div>
      </div>
    </div>
  </div>

</template>


<script>

import UIButton from "@/components/views/UIButton.vue"

export default {
  name: "ProjectCard",
  components: {UIButton},
  data() {
    return {
    };
  },

  props: {
    title: String,
    img: String,
    tag: String,
    city: String,
    path: String
  },

  created() {
  },

  mounted() {


  },


  methods: {
    onPath() {
      this.$router.push(this.path);
    }
  }
}
</script>