<template>
  <div>
    <HeaderView v-bind:title="title" v-bind:description="description" />
    <Contents v-bind:contents="contents" />
  </div>
</template>

<script>
import HeaderView from "../HeaderView.vue";
import Contents from "./Contents.vue";

export default {
  components: {
    HeaderView,
    Contents
  },
  props: {
    initialData: {
      type: Object,
      default: () => {}
    }
  },
  data() {
    return {
      title: this.initialData.title,
      description: this.initialData.description,
      contents: this.initialData.contents
    }
  },
};
</script>

<style scoped></style>
