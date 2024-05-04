<template>
  <div class="container">
    <!-- Elemen teks statis -->
    <h1>Halo, Ini Contoh Halaman Web dengan Vue.js</h1><br>
    
    
    <!-- Elemen input teks dengan penggunaan class bindings dan style bindings -->
    <input type="text" v-model="inputText" :class="{ 'highlight': isHighlighted }" :style="{ 'font-weight': isBold ? 'bold' : 'normal' }">
    
    <!-- Elemen dinamis yang menggunakan nilai dari data Vue -->
    <p v-if="inputText !== ''">Anda mengetik: {{ inputText }}</p>
    
    <!-- Tombol untuk mengubah nilai data Vue secara dinamis -->
    <button @click="toggleHighlight">Toggle Highlight</button>
    <button @click="toggleBold">Toggle Bold</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputText: '', // Nilai dari input teks
      isHighlighted: false, // Status highlight
      isBold: false // Status bold
    };
  },
  methods: {
    // Metode untuk mengubah status highlight
    toggleHighlight() {
      this.isHighlighted = !this.isHighlighted;
    },
    // Metode untuk mengubah status bold
    toggleBold() {
      this.isBold = !this.isBold;
    }
  }
};
</script>

<style>


.container {
  background-image: linear-gradient(to bottom right, #8e44ad, #3498db);
  color: white;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  /* transition: background 0.3s ease; */
  
}

/* .container :hover{
  background: linear-gradient(to bottom right, #3498db, #8e44ad)
} */

.highlight {
  background-color: rgba(255, 255, 0, 0.5);
}
</style>
