<template>
  <div>
    <input
      class="ar-input"
      :style="size"
      :placeholder="placeholder"/>
  </div>
</template>

<script>
export default {
  data() {
    return {}
  },

  computed: {
    size() {
      const width = this.width;
      const height = this.height;
      if (!width && !height) {
        return Object.assign({}, { width: '178px', height: '38px'})
      }
      if (width && !height) {
        return Object.assign({}, { width: `${width}px`, height: '38px'})
      }
      if (!width && height) {
        return Object.assign({}, { width: '178px', height: `${height}px`})
      }
      if (width && height) {
        return Object.assign({}, { width: `${width}px`, height: `${height}px`})
      }
    },
  },

  props: {
    placeholder: {
      type: String,
      default: null,
    },
    width: {
      type: Number,
      default: null,
    },
    height: {
      type: Number,
      default: null,
    },
  },

}
</script>

<style lang="scss" scoped>
@import './styles/mixin.scss';
.ar-input{
  border-radius: 3px;
  border: solid 1px $mainB;
  padding: 0 30px 0 15px;
  transition: all .2s cubic-bezier(.645,.045,.355,1);
  &:hover{
    border-color: $hoverB;
  }
  &:focus{
    outline: none;
    border-color: $theme;
  }
}
</style>
