<template>
  <div class="small-vertical-post">
    <div class="card">
      <img :src="url_img" class="card-img" />
      <div class="card-body p-0">

        <nuxt-link  :to="'visualmag-pro/'+h5">         <h5 href="" style="color: black;"> {{ h5 }}   </h5></nuxt-link>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: ["url_img", "h5"],
};
</script>
 <style scoped>
.card {
  border: none;
  color: black;
}
h5 {
    margin: 0;
  font-size: 17px;
  margin-top: 18px;
  color: black;
}
.card-img {
  width: 100%;
  object-fit: cover;
}
img {
  float: left;
}
</style>