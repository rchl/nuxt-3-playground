<template>
  <div :class="bar" @click="foo"></div>
  <nuxt-link to="/" role="foo" />
</template>
<script>
export default {
  async serverPrefetch() {
    this.foo();
    this.bar = 'baz'
  },
  mounted() {
    this.foo();
    this.bar = 'baz'
  },
  data() {
    return {
      bar: 'bar'
    };
  },
  methods: {
    /** @returns {number} */
    foo() {
      return 1
    }
  }
};
</script>
