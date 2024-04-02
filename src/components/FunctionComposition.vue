<template>
  <div class="border-b">
    <h2 class="mb-12">Solution no 2</h2>
    <p>Result: {{ composedResult }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      composedResult: 0,
    };
  },
  mounted() {
    this.composeFunctions();
  },
  methods: {
    addOne(x) {
      return x + 1;
    },
    multiplyByTwo(x) {
      return x * 2;
    },
    subtractThree(x) {
      return x - 3;
    },
    composeFunctions() {
      const addOne = this.addOne;
      const multiplyByTwo = this.multiplyByTwo;
      const subtractThree = this.subtractThree;

      const result = subtractThree(multiplyByTwo(addOne(5)));
      this.composedResult = result;
    },
  },
};
</script>
