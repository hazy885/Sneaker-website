<template>
  <topbar />
  <!-- Main Content -->
  <div class="home-page-container">
   

    <div class="card-container">
      <div class="card" :style="cardStyle">
        <div class="card-face card-face--front">
          <slot name="front">Front Side</slot>
        </div>
        <div class="card-face card-face--left">
          <slot name="left">Left Side</slot>
        </div>
        <div class="card-face card-face--right">
          <slot name="right">Right Side</slot>
        </div>
      </div>
      <div class="button-container">
        <button class="flip-button flip-button--left" @click="rotateLeft">Rotate Left</button>
        <button class="flip-button flip-button--right" @click="rotateRight">Rotate Right</button>
      </div>
    </div>
    <!-- Featured Products Section -->
    <!-- <section class="featured-products">
      <h2>Featured Shoes</h2>
      <div class="product-list">
        <div class="product-card">
          <img src="../images/Nike Air Jordan 1 Custom.jpg" alt="Shoe 1">
          <h3>Running Sneakers</h3>
          <p>$120.00</p>
        </div>
        <div class="product-card">
          <img src="../images/Nike Air Force 1 Rocafella.jpg" alt="Shoe 2">
          <h3>Classic Loafers</h3>
          <p>$90.00</p>
        </div>
        <div class="product-card">
          <img src="../images/Air Jordan 1 High OG x Dior 1.jpg" alt="Shoe 3">
          <h3>Formal Oxfords</h3>
          <p>$150.00</p>
        </div>
      </div>
    </section> -->
    <!-- Footer -->
  </div>
  <TheFooter />
</template>

<script setup>
import { ref, computed } from 'vue'


const currentRotation = ref(0)

const cardStyle = computed(() => ({
  transform: `rotateY(${currentRotation.value}deg)`
}))

const rotateLeft = () => {
  currentRotation.value -= 120
}

const rotateRight = () => {
  currentRotation.value += 120
}
</script>

<style></style>