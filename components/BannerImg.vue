<template>
  <div class="banner-img-container">
      <img :src="url_img" alt="" />
      <div class="text-overlay">
        <h1 v-if="disable_h1">{{ h1 }}</h1>
        <div v-else></div>
        <h4>{{ h4 }}</h4>
      </div>
  </div>
</template>
<script>
export default {
  props: ["url_img", "h1", "color", "h4", "disable_h1"],
};
</script>
<style scoped>
* {
  padding: 0;
  margin: 0;
  color: white;
}
.banner-img-container {
  display: flex;
  overflow: hidden;
  position: relative
}
.text-overlay {
  position: absolute;
  bottom: 20px;
  left: 20px;
  box-sizing: border-box;
}
.text-overlay:hover {
  color: white;
}
h1 {
  display: inline;
  font-family: "Inter";
  padding: 3px 6px 3px;
  background-color: #34bf49;
  font-weight: 400;
  font-size: 11px;
}
h4 {
  font-family: sans-serif;
  font-weight: 700;
  margin: 0;
  overflow-wrap: break-word;
  word-wrap: break-word;
  word-break: break-word;
  font-size: 17px;
  padding-top: 8px;
  padding-right: 20px;
}
img {
  filter: brightness(80%);
  width: 100%;
  display: block;
  min-width: 100%;
  min-height: 100%;
}
</style>