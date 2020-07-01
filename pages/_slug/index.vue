<template>
  <div class="container">
    <nuxt-content :document="page" />
  </div>
</template>

<script>
export default {
  async asyncData({ params, $content }) {
    const page = await $content('post', params.slug).fetch()
    return {
      page,
    }
  },
}
</script>

<style></style>
