<template>
<div>
  <h1>Users</h1>
  <div>
    <input type="text" v-model="userID">
    <button @click="onLoadUser">Load User</button>
  </div>
  <nuxt-child />
</div>
</template>

<script>
export default {
  data(){
    return {
      userID: ''
    }
  },
  methods: {
    onLoadUser(){
      this.$router.push(`/users/${this.userID}`)
    }
  },
  layout: 'users'
}
</script>
