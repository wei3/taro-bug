<template>
  <view class="index" @tap="showText">
    <text >{{ msg }}</text>

    <text v-if="isShow">我可以隐藏/显示</text>
  </view>
</template>

<script>
import { ref } from 'vue'
import './index.scss'

export default {
  setup () {
    const msg = ref('Hello world')
    return {
      msg,
      isShow : false
    }
  },
  methods : {
    showText(){
      console.log(this.isShow)
      this.isShow = true;
    }
  }
}
</script>
