<template>
  <div class="clock">
    <h1>{{ currentTime }}</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentTime: new Date().toLocaleTimeString()
    };
  },
  created() {
    setInterval(() => {
      this.currentTime = new Date().toLocaleTimeString();
    }, 1000);
  }
};
</script>

<style>
.clock {
  text-align: center;
  font-size: 2rem;
  margin-top: 2rem;
}
</style>