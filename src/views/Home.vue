<template>
  <div class="col-full">
    <h1>Welcome to the Foroom</h1>
    <ThreadList :threads="threads"/>
  </div>
</template>

<script>
import sourceData from '@/data'
import ThreadList from '@/components/ThreadList'

export default {
  name: 'Home',

  components: {
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
</script>
