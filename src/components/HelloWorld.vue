<template>

  <div class="col-full">
        <h1>welcome to the Forum</h1>
        <ThreadList :threads="threads"/>
   
  <!-- <div>
    <h1>Welcome to the Forum</h1>
    <div v-for="thread in threads">
      <h2>{{thread.title}}</h2>
        <div v-for="postId in thread.posts">
          <p>{{users[posts[postId].userId].name}}</p>
          <p>{{posts[postId].text}}</p>
      </div>
    </div>
  </div> -->
  
  </div>
</template>

<script>

import sourceData from '@/data'
console.log(sourceData.threads)

import ThreadList from './ThreadList'

export default {
  name: 'HelloWorld',

  components:{
    ThreadList
  },

  data () {
    return {
      threads: Object.values(sourceData.threads),
      posts: sourceData.posts,
      users: sourceData.users
    }
  }
}
console.log('>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>')
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
