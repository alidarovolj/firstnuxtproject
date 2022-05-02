<template>
  <div>
    <div v-if="$fetchState.pending" class="w-full h-full">
      <div class="preloader">
        <div class="relative w-full h-full">
          <div class="setSpinner">
            <div class="lds-dual-ring">
              <div></div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <p v-else-if="$fetchState.error">
      An error occurred :(
    </p>
    <div v-else>
      <h1>Nuxt Mountains</h1>
      <ul>
        <li v-for="mountain of mountains" :key="mountain.id">
          {{ mountain.title }}
        </li>
      </ul>
      <button @click="$fetch">
        Refresh
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FetchData',
  data () {
    return {
      mountains: []
    }
  },
  async fetch () {
    this.mountains = await fetch(
      'https://api.nuxtjs.dev/mountains'
    ).then(res => res.json())
  }
}
</script>

<style scoped>
  .preloader {
    position: fixed;
    width: 100%;
    height: 1000px;
    left: 0;
    top: 0;
  }
  .setSpinner {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
  }
</style>
