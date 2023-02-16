<template>
  <div>
    <h1>UploadCare Demo</h1>
    <Uploadcare
      publicKey="22f2e7409df884f51531"
      v-bind:imagesOnly="true"
      tabs="dropbox"
      v-bind:multiple="true"
      v-on:success="processUploadImage"
    >
      <button>Upload</button>
    </Uploadcare>
  </div>
</template>

<script>
import Uploadcare from "uploadcare-vue";
export default {
  name: "App",
  methods: {
    async processUploadImage(params) {
      //   const response = await axios.post(baseAPIUrl + "images", {
      //     name: params.name,
      //     url: params.cdnUrl,
      //   });
      //   console.log(response.data);
      console.log(params);
    },
  },
  components: {
    Uploadcare,
  },
  //   data() {
  //     return {
  //       MY_API_KEY: "22f2e7409df884f51531",
  //     };
  //   },
};
</script>

<style></style>

<!-- 
      v-bind:previewStep="true"
      imageShrink="1440x1080"
-->
