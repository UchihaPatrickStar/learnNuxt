<template>
  <div>
    <h2>News-content</h2>
    <p>NewsId: {{$route.params.id}}</p>
    <ul>
      <li><a href="/">Home</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  validate({params}) {
    return /^\d+$/.test(params.id)
  },
  data() {
    return {
      title: this.$route.params.title
    }
  },
  head() {
    return {
      title: this.title,
      meta: [
        {hid: 'description', name: 'news1',content: 'This is news page'}
      ]
    }
  }
}
</script>