<template>
  <ul>
    <li v-for="option in options" :key="option.id">
      <p>{{ option.value }}</p>
    </li>
  </ul>
</template>

<style lang="scss" scoped>
</style>

<script lang="ts">
import { Component, Prop, Vue, Watch } from "vue-property-decorator";
import { optionModule } from '../store/module/Option';

@Component
export default class ExampleComponent extends Vue {

  private mounted(): void {
    console.log("mounted");
  }

  get options() {
    return optionModule.options;
  }
}
</script>
