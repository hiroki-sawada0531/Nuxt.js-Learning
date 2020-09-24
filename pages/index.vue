<template>
  <div class="container">
    <div>
    <div v-if="isActive === false" v-on:click="hoge()" class="test1">{{ msg }}</div>
    <div v-if="isActive === true" v-on:click="hoge()" class="test2">{{ msg }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      msg: "アイウエオ",
      isActive: false
    }
  },
  methods: {
    hoge(){
    if(this.isActive === true) {
      this.isActive = false;
      } else {
      this.isActive = true;
      }
    }
  }
}

</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.test1 {
width:500px;
height:500px;
background-color: aqua;
}

.test2 {
width:500px;
height:500px;
background-color:rgba(247,31,66);
}
</style>