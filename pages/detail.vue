<template>
  <div class="container">
    <h1>{{ msg }} </h1>
    <span>{{ hello }}</span>
    <!-- <button @click="$store.commit('increment')">{{ $store.state.counter }}</button> -->
  </div>
</template>
<script>
import { mapState, mapMutations } from 'vuex'
import axios from 'axios'

export default {
  // asyncData({isDev, route, store, env, params, query, req, res, redirect, error}) {
  //   msg: 'detail page'
  // },
  async asyncData(context, params = {id: 232}) {
    // let { data } = await axios.get(`https://my-api/posts/${params.id}`)
    return {
      msg: 'msg data',
      title: 'data.title'
    }
  },
  data() {
    return {
      hello: 'hello'
    }
  },
  head: {
    meta: [
      { charset: 'utf-8' },
      { name: 'viewport', content: 'width=device-width, initial-scale=1' }
    ],
    link: [
      { rel: 'stylesheet', href: 'https://fonts.googleapis.com/css?family=Roboto' }
    ]
  },

}
</script>
<style lang="css">
div {
  color: red;
}
</style>
