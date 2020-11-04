<template>
  <div class="grid">
    <input type="text" v-model="result" placeholder="0">
    <button class="cell num" @keyup.enter="calc()" @click="input(num)" v-for="num in numbers" :key="num.id">{{ num }}</button>
    <button class="cell op" @click="input(op)" v-for="op in operations" :key="op.id">{{ op }}</button>
    <button class="cell op" @click="reset()">R</button>
    <button class="cell op" @click="calc()">=</button>
  </div>
</template>

<script>
export default {
  name: 'Calculate',
  data() {
    return {
      result: '',
      numbers: [1, 2, 3, 4, 5, 6, 7, 8, 9, 0],
      operations: ['+', '-', '*', '/']
    }
  },
  methods: {
    input(char) {
      this.result = this.result.toString()
      this.result+=char
    },
    reset() {
      this.result = ''
    },
    calc() {
      this.result = Math.trunc(eval(this.result))
    }
  }
}
</script>


<style scoped>
input[type="text"] {
  width: 200px;
  border: 0;
  color: #243849;
  font-size: 18px;
  padding: 5px 5px;
  text-align: right;
}
.grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  width: 100%;
}
.cell {
  flex: 33%;
  height: 50px;
  font-size: 18px;
  border: none;
}
.num {
  background-color: #243849;
  color: #fff;
  font-weight: 400;
  cursor: pointer;
}
.cell:hover{
  background-color: #182530;
}
.op {
  background-color: #ff9900;
  color: #243849;
  cursor: pointer;
}
.op:hover {
  color: #fff;
}

</style>
