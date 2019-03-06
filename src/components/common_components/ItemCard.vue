<template>
  <div class="container">
    <b-card :title="item.Title"
            img-src="https://picsum.photos/600/300?image=1073"
            img-alt="Image"
            img-top
            tag="article"
            style="max-width: 20rem;"
            class="mb-2 text-center">
      <p class="card-text">
        Author: {{item.Author}}
      </p>
      <hr>
      <p>Price: ${{item.Price}}</p>
      <hr>
      <b-button variant="info" @click.prevent="updateCart(item)"><v-icon name="cart-plus" /> </b-button>
      <b-button variant="primary" @click="details(item.Title)"><v-icon name="list" /> </b-button>
    </b-card>
  </div>
</template>

<script>
export default {
  name: 'ItemCard',
  props: ['item', 'updateCart'],
  methods: {
    details (title) {
      this.$router.push('/products/' + title)
    }
  }
}
</script>

<style scoped>

</style>
