<template>
  <div class="container">
    <h1>Compute Product</h1>
    
    <div class="image-container">
      <img src="https://i.pinimg.com/736x/3b/40/1c/3b401ceb37213d3409fb4d8d392204db.jpg" alt="Task Image" class="task-image">
    </div>
    
    <div class="numbers">
      <p>First number: {{ num1 }}</p>
      <p>Second number: {{ num2 }}</p>
    </div>
    
    <button v-if="!showResult" @click="calculateProduct" class="compute-btn">
      Compute
    </button>
    
    <div v-if="showResult" class="result">
      <p>The product of {{ num1 }} and {{ num2 }} is {{ product }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num1: 5,
      num2: 7,
      product: 0,
      showResult: false
    }
  },
  methods: {
    calculateProduct() {
      this.product = this.num1 * this.num2;
      this.showResult = true;
    }
  }
}
</script>

<style>
.container {
  font-family: Arial, sans-serif;
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
  text-align: center;
}

h1 {
  color: #333;
  margin-bottom: 20px;
}

.task-image {
  max-width: 100%;
  height: auto;
  margin: 20px 0;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.numbers {
  background-color: #f5f5f5;
  padding: 15px;
  border-radius: 8px;
  margin-bottom: 20px;
}

.compute-btn {
  background-color: #4CAF50;
  color: white;
  border: none;
  padding: 10px 20px;
  font-size: 16px;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.compute-btn:hover {
  background-color: #45a049;
}

.result {
  background-color: #e6f7ff;
  padding: 15px;
  border-radius: 8px;
  font-weight: bold;
  font-size: 18px;
}
</style> 