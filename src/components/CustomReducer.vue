<template>
  <div class="p-5">
    <h2 class="mb-12">Solution no 3</h2>
    <p class="m-0">Final result: {{ finalResult }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      finalResult: 0,
    };
  },
  mounted() {
    this.customReduce();
  },
  methods: {
    sumReducer(acc, num) {
      return acc + num;
    },
    customReduce() {
      const nums = [1, 2, 3, 4, 5];
      const init = 0;
      let result = init;
      for (let i = 0; i < nums.length; i++) {
        result = this.sumReducer(result, nums[i]);
      }
      this.finalResult = result;
    },
  },
};
</script>
