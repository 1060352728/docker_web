
<script setup>
import axios from 'axios';
import {ref} from "vue";

const count = ref()
const getData = () => {
  axios.get('/test/getDate')
      .then(response => {
        count.value = response.data
      });
}
</script>

<template>
  <div>
    <button @click="getData">点击获取后台参数</button>
  </div>
  <div><textarea>{{count}}</textarea></div>
</template>

<style scoped>

</style>
