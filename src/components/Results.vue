<template>
  <div class="showresult">
    <p>Reaction time: {{ score }} ms</p>
    <p class="rank">{{ rank }}</p>
  </div>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score < 250) {
      this.rank = "Flash fingers ⚡";
    } else if (this.score < 400) {
      this.rank = "Good Reflex ";
    } else {
      this.rank = "Slow snail";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4em;
  color: #0faf84;
  font-weight: bold;
}
</style>
