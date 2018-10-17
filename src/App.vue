<template>
  <div id="app">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div> -->

    <router-view/>
    <mt-tabbar v-model="selected" v-on:click.native="select" >
        <mt-tab-item id="home">
          <img slot="icon" src="./assets/minlogo.png">
          外卖
        </mt-tab-item>
        <mt-tab-item id="search">
          <img slot="icon" src="./assets/minlogo.png">
          搜索
        </mt-tab-item>
        <mt-tab-item id="order">
          <img slot="icon" src="./assets/minlogo.png">
          订单
        </mt-tab-item>
        <mt-tab-item id="me">
          <img slot="icon" src="./assets/minlogo.png">
          我的
        </mt-tab-item>
      </mt-tabbar>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
  },
  computed: {

  },
  data() {
    return {
      selected: "home",
    }
  }, 
  created: {
    
  },
  methods: {
    select () {
      // console.log(this.selected)
      
      this.$router.push(this.selected);
    },
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  /* color: #2c3e50; */
  /* margin-top: 0px; */
  margin: 0px;
  background-color: blue;
}
#content{
  position: absolute;
  margin: 0px;
  top: 0px;
  left: 0px;
  width: 100%;
  height: 100%;
  background-color: rgb(255, 127, 148);
}

</style>
