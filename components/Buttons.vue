<template>
  <div
    v-editable="blok"
    :style="{justifyContent: blok.alignment}"
    class="Buttons">
    <component
      v-for="blok in blok.buttons"
      :key="blok._uid"
      :blok="blok"
      :is="'vue-' + blok.component"/>
  </div>
</template>

<script>
  export default {
    props: {
      blok: {
        type: Object,
        default: function () {
          return {}
        }
      }
    },
  }
</script>
