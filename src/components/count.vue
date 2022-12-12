<template>
  <div class="wrap"> 
    <h3>当前的和为：{{sum}}</h3>
    <select class="btn" v-model.number="n">
        <option v-for="(value, index) of optionsArr" :key="index" :value="value">{{value}}</option>
    </select>
    <button class="btn" @click="addHandler">+</button>
    <button class="btn" @click="subHandler">-</button>
    <button class="btn" @click="oddAddHandler">当前和为奇数再加</button>
    <button class="btn" @click="weitAddHandler">等等再加</button>
  </div>
</template>

<script>
export default {
  name: 'CountComponent',
  data() {
    return {
      n:1,
      optionsArr: [1, 2, 3, 4, 5],
      sum: 0
    }
  },
  methods: {
    addHandler() {
      this.sum += this.n;
    },

    subHandler() {
      this.sum -= this.n;
    },

    oddAddHandler() {
      if (!(this.sum % 2)) return;
      this.sum += this.n
    },

    weitAddHandler() {
      setTimeout(() => {
        this.sum += this.n
      }, 300)
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .btn{
    margin-left: 5px
  }
  .wrap{
    background: aqua;
  }
</style>
