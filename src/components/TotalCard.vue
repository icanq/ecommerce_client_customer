<template>
  <div class="card">
  <header class="card-header">
    <p class="card-header-title">
      Component
    </p>
    <a href="#" class="card-header-icon" aria-label="more options">
      <span class="icon">
        <i class="fas fa-angle-down" aria-hidden="true"></i>
      </span>
    </a>
  </header>
  <div class="card-content">
    <small>total price:</small>
    <h5>{{ totalPrice }}</h5>
  </div>
  <footer class="card-footer">
    <button @click.prevent="checkout" class="card-footer-item">checkout</button>
  </footer>
</div>
</template>

<script>
export default {
  name: 'TotalCard',
  props: ['totalPrice'],
  methods: {
    checkout () {
      this.$store.dispatch('checkoutCarts')
    }
  }
}
</script>

<style>

</style>
