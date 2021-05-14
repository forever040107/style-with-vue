<template>
  <Wrapper>
    <input :name="name" type="checkbox" :checked="isChecked" @change="onChange">
    <div class="label">change to Grid</div>
  </Wrapper>
</template>

<script>
import { Wrapper } from "./Styled.js";
export default {
  props: {
    name: String,
    isChecked: Boolean,
    label: String
  },
  components: {
    Wrapper
  },
  methods: {
    onChange() {
      console.log("#####");
      this.$emit("change");
    }
  }
};
</script>
