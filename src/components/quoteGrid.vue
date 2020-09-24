<template>
  <div class="row">
    <qoute-cmp v-for="(qt , index) in quotes" :key="index" @click.native="deleteQouteFn(index)">{{ qt }}</qoute-cmp>
  </div>
</template>

<script>
import Quote from "./quote.vue";
export default {
  props: ["quotes" , "deleteQouteFn"],
  components: { "qoute-cmp": Quote },
};
</script>

<style scoped>
</style>