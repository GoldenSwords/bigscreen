<template>
  <el-color-picker
    :disabled="disabled"
    v-model="color"
    size="mini"
    :show-alpha="true"
    @change="change"
  ></el-color-picker>
</template>

<script>
export default {
  name: "LColor",
  props: {
    value: String,
    disabled: Boolean,
    option: Object
  },
  watch: {},
  beforeMount() {
    this.color = this.value;
  },
  mounted() {},
  methods: {
    change(val) {
      this.$emit("callback", val);
    }
  },
  data() {
    return {
      color: "#409EFF"
    };
  }
};
</script>

<style scoped></style>
