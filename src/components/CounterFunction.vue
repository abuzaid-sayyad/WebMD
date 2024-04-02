<template>
  <div class="border-b">
    <p>Current value: {{ currentValue }}</p>
    <button @click="increment">Increment</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentValue: 0,
    };
  },
  methods: {
    increment() {
      this.currentValue++;
    },
  },
};
</script>

<style scoped>
.border-b{
  border-bottom: 1px solid #e5e7eb;
  padding: 30px;
}
.border-b  p{
  margin: 0 0 12px;
}
.border-b button{
  background: #22c55e;
  padding: 10px 24px;
  color: #ffffff;
  font-size: 14px;
  font-weight: 600;
  border: none;
  outline: none;
  border-radius: 8px;
  cursor: pointer;

}
</style>
