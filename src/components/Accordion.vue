<template>
  <div class="accordion">
    <div
      class="accordion__item"
      v-for="item in accordionItems"
      :key="item.title"
      v-bind:class="{active:item.isActive}"
    >
      <div class="accordion__title" @click="toggleAccordion(item)">{{ item.title }}</div>
      <div class="accordion__content" v-if="item.active">{{ item.content }}</div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["accordionItems"],
  methods: {
    toggleAccordion(curr) {
      curr.active = !curr.active;
    }
  }
};
</script>

<style lang='scss'>
.accordion {
  &__title {
    padding: 10px;
    background-color: grey;
  }
}
.actice {
  background-color: purple;
}
</style>
