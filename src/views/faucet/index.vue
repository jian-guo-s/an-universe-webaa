<template>
<div>
  <h1>水龙头页面</h1>
  <vue-recaptcha
      :sitekey="v2Sitekey"
      size="normal"
      theme="light"
      hl="zh-TW"
      @verify="recaptchaVerified"
      @expire="recaptchaExpired"
      @fail="recaptchaFailed"
  >
  </vue-recaptcha>
</div>
</template>

<script lang="ts" setup>
import vueRecaptcha from 'vue3-recaptcha2';
const v2Sitekey = '6LcWvccpAAAAAHcR20JmIy_Zq9NKiYba72YWqQ75';
const recaptchaVerified = (res) => {
  console.log(res)
}

const recaptchaExpired = () => {
  // 過期後執行動作
}

const recaptchaFailed = () => {
  // 失敗執行動作
}
</script>

<style scoped>

</style>