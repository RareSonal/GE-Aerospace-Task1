<script setup>
import { ref } from 'vue'

const heading = ref('Compute Product')

// Numbers to be multiplied
const num1 = ref(5)
const num2 = ref(10)

// Variable to store the product
const product = ref(null)

// Function to compute the product
const computeProduct = () => {
  product.value = num1.value * num2.value
  showButton.value = false
}

// Flag to control button visibility
const showButton = ref(true)
</script>

<template>
  <!-- Main heading -->
  <h2>{{ heading }}</h2>

  <!-- Embed image from Unsplash -->
  <img 
    src="https://images.unsplash.com/photo-1436491865332-7a61a109cc05?q=80&w=1474&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" 
    alt="Plane window overlooking sea of clouds"
    width="400" 
    height="300" 
  />

  <!-- Display the numbers to be multiplied -->
  <p>Number 1: {{ num1 }}</p>
  <p>Number 2: {{ num2 }}</p>

  <!-- Button to trigger the computation -->
  <button v-if="showButton" @click="computeProduct">Compute</button>

  <!-- Display the product of the numbers -->
  <p v-if="product !== null">Product: {{ product }}</p>
</template>
