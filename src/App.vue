<template>
  <h1 @click="increase">{{ count }}</h1>
  <div v-if="count > 4">4보다 큽니다!</div>
  <ul>
    <li v-for="fruit in fruits" :key="fruit" :name="fruit">{{ fruit }}</li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
      fruits: ["Apple", "Banana", "Cherry"],
    };
  },
  methods: {
    increase() {
      this.count += 1;
    },
  },
};
</script>

<style lang="scss">
h1 {
  font-size: 50px;
  color: royalblue;
}

ul {
  li {
    font-size: 50px;
  }
}
</style>
