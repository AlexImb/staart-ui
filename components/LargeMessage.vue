<template>
  <div>
    <img alt="" src="https://undraw.oswaldlabs.com/super-thank-you.svg" />
    <h1>{{ heading }}</h1>
    <p>{{ text }}</p>
    <nuxt-link
      v-if="ctaText && ctaTo"
      class="button button--size-large button--color-primary section section--mt-1"
      :to="ctaTo"
      >{{ ctaText }} &rarr;</nuxt-link
    >
  </div>
</template>

<script lang="ts">
import { Component, Vue, Prop } from "vue-property-decorator";

@Component({})
export default class LargeMessage extends Vue {
  @Prop() heading;
  @Prop() text;
  @Prop() ctaText;
  @Prop() ctaTo;
}
</script>

<style lang="scss" scoped>
div {
  text-align: center;
}
h1 {
  font-size: 200%;
  font-weight: 300;
}
img {
  max-width: 200px;
}
</style>
