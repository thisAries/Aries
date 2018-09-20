<template>
  <div class="thisAries">
    <div class="input">
      <label>
        <a>ar-input</a>
        <Input :width="200" :height="42"/>
      </label>
    </div>
  </div>
</template>

<script>
import Input from './Input';
export default {
  name: 'app',
  data() {
    return {}
  },
  components: {
    Input,
  },
}
</script>

<style lang="scss">
.thisAries{
  display: flex;
  width: 100vw;
  height: 100vh;
}
</style>
