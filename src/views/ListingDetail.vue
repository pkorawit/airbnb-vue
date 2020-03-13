<template>
  <h1>Listing Detail {{ id }}</h1>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      id: this.$route.params.id
    };
  },
  mounted() {
    let url =
      "https://airbnbapidemo.azurewebsites.net/api/airbnb/listings/";
    url = url + this.id;
    axios.get(url).then(response => {
      console.log(response.data);
      
    });
  }
};
</script>

<style>
</style>