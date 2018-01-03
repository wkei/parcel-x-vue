<template>
  <div class='container'>
    <Header />
    <article class="article">
      <p>{{msg}}</p>
    </article>
    <button @click='halo'>Halo</button>
  </div>
</template>

<script>
import Header from './components/Header.vue'

export default {
  data () {
    return {
      msg: 'Halo'
    }
  },
  components: {
    Header
  },
  created () {
    console.log('App.vue is created')
  },
  methods: {
    halo () {
      this.msg = `× ${this.msg} ×`
    }
  }
}
</script>

<style lang='scss'>
@import 'styles/base';
@import 'styles/vars';
$gutter: 15px;

.container {
  padding: $gutter * 2 $gutter;
  text-align: center;
  .article {
    color: $blue;
  }
}
</style>
