<template>
  <div class="count">
    <h1>Counter</h1>
    <div>
      <button @click="decreaseCounter" class="btn">-</button>
      <span class="counter">{{counter}}</span>
      <button @click="increaseCounter" class="btn">+</button>     
    </div>
    <div>
      <li>Game</li>
      <li>Game</li>
      <li>Game</li>
      <li>Game</li>
      <li>Game</li>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      counter: 0 
    }
  },
  methods : {
    increaseCounter() {
      this.counter++
    },
    decreaseCounter() {
      this.counter--
    }
  }
}
</script>

<style>
.count {
  text-align: center;
  padding: 20px;
}
.btn ,.counter {
  font-size: 40px;
  margin: 10px;
}
.btn {
  background: aquamarine ;
  border-radius: 30px;
}
</style>