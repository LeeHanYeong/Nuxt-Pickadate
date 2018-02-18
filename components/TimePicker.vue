<template>
  <input id="timepicker" v-model="value" type="text">
</template>

<script>
import $ from 'jquery'

export default {
  props: ['value'],
  mounted () {
    // 이거는 잘 됨
    console.log($('#timepicker'))
    console.log($(this.$el))

    // 이거는 안 됨
    // pickadate js모듈을 어떻게 불러와야 하는지 모르겠음
    // npm install pickadate로 설치 가능
    
    // $('#timepicker').pickatime()
    $(this.$el).pickatime()
  }
}
</script>