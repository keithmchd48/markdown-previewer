<template>
  <div id="app">
    <i-container class="container">
      <i-row>
        <i-column class="border-right" sm="6">
          <h1>Markdown</h1>
          <i-textarea rows="7" v-model="text" placeholder="Type something..." />
        </i-column>
        <i-column sm="6">
          <h1>Formatted Text</h1>
          <VueMarkdown :source="text">
          </VueMarkdown>
        </i-column>
      </i-row>
    </i-container>
  </div>
</template>

<script>
  import VueMarkdown from 'vue-markdown'
export default {
  name: 'App',
  data () {
    return {
      text: ''
    }
  },
  components: {
    VueMarkdown
  }
}
</script>

<style>
  .container {
    margin-top: 40px;
  }
  .border-right {
    border-right: 1px solid;
  }
</style>
