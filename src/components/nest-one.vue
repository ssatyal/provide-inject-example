<template>
  <nest-two :msg="msg"/>
</template>

<script>
import NestTwo from './nest-two.vue';
export default {
  name: 'NestOne',
  components: {
    NestTwo,
  },
  props: {
    msg: String
  }
}
</script>