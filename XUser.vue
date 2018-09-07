<template>
  <span class="wrapper">
    <img :src="avatarUrl" alt="User avatar" class="avatar">
    <a :href="userUrl">@{{username}}</a>
  </span>
</template>

<script>

export default {
  name: 'XUser',
  props: ['username'],
  computed: {
    avatarUrl () { return `https://avatars.io/twitter/${this.username}`; },
    userUrl () { return `https://twitter.com/${this.username}`; }
  }
}
</script>

<style>
.wrapper {
  display: grid;
  grid-template-columns: auto auto;
  grid-column-gap: 1ch;
  align-items: center;
  font-family: monospace;
}
.avatar {
  border-radius: 50%;
  width: 2rem;
  height: 2rem;
}
</style>
