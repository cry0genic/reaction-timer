<template>
  <p>Reaction Time: {{score}} ms</p>
  <p class="rank"> {{rank}}</p>
</template>

<script>
export default {
  props: ['score'],
  data() {
    return {
      rank: null
    }
  },
  mounted() {
    if (this.rank <250){
      this.rank = 'Ninja fingers'
    } else if (this.rank < 400){
      this.rank = 'Rapid reflexes'
    } else {
      this.rank = 'Snail pace'
    }
  }
}
</script>

<style>
.rank {
  font-size: 1.4em;
  color: #0faf87;
  font-weight: bold;
}
</style>