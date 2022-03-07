<template>
    <div class="navigation">
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
      </ul>
    </div>
</template>

<script>
export default {
  name: 'Sidebar',
  data () {
    return {
      opened: false
    }
  },
  methods: {
    closeNav () {
      this.opened = false
    },
    openNav () {
      this.opened = true
    }
  }
}
</script>

<style>
.navigation {
  float: left;
}
ul {
  list-style-type: none;
}
</style>
