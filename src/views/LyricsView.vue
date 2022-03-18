<template>
  <div class="result" v-for="lyric of lyrics" :key="lyric">
        <h2 class="text-center mb-2">{{artist}}</h2>
        <div class="mt-4">{{lyrics}}</div>
      </div>
</template>

<script>
export default {
  data () {
    return {
      lyric: '',
    };
  },
  methods: {
    async obtenerLyrics() {
      try {
        const data = await fecth(`https://api.lyrics.ovh/v1/${this.artist}/${this.lyrics}`);
        const getLyrics = await data.json();
        this.lyrics = getLyrics.results;
      } catch (error) {
        throw error;
      }
    },
  },
  created() {
    this.obtenerLyrics();
  }
}
</script>

<style>

</style>