<template>
  <div class="app" :class="mode">
    <toggle :mode="mode" @toggle="toggle" />
    <div class="container">
      <card :mode="mode" />
    </div>
  </div>
</template>

<script>
import Card from '@/components/Card.vue';
import Toggle from '@/components/Toggle.vue';

export default {
  name: 'App',
  data(){
    return{
      mode: 'light'
    }
  },
  components: {
    Card,
    Toggle
  },
  methods: {
    toggle(){
      if(this.mode === 'dark' ){
        this.mode = "light"
      }else{
        this.mode = "dark"
      }
    }
  }
}
</script>

<style>
  :root{
    --sand: #e3dbe3;
    --light-green: #9cb2a5;
    --light-blue: #8ba4b3;
    --light-pink: #c8b7c9;
    --old-pink: #9d7982;
    --red-wine: #733236;

    /* dark mode */

    --dark: #181a31;
    --dark-blue: #282f4b;
    --blue: #434f75;
  }
  *{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }
  .app {
    
    font-family: 'Roboto', sans-serif;
    background-image: linear-gradient(to right top, #8ba4b3, #8aa8b2, #8babaf, #8eaeac, #93b0a9, #98b5b0, #9db9b7, #a3bebe, #b0c5ce, #c2ccd8, #d4d3df, #e3dbe3);
    width: 100%;
    min-height: 100vh;
    transition: background-image 0.3s ease-in-out;
  }
  .container{
    width: 100%;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .dark{
    background-image: linear-gradient(to right top, #181a31, #1b1e36, #1e223a, #21263f, #242a44, #282e4a, #2b334f, #2f3755, #343d5d, #394365, #3e496d, #434f75);
    transition: background-image 0.3s ease-in-out;
  }

</style>
