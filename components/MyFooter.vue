<template>
<footer class="footer has-text-light">
  <div class="container">
    <div class="columns">
      <div class="column is-2 has-text-centered">
        <img src="/imgs/logos/Buet_logo.svg" style="max-height: 125px;">
      </div>
      <div class="column content">
        <vue-markdown>
Nasif Zaman

Computer Science and Engineering Graduate

Bangladesh University of Engineering and Technology

[nasifzaman@yahoo.com](nasifzaman@yahoo.com)
        </vue-markdown>
      </div>
      <div class="column">
        <vue-markdown>
*Borrowed by Nasif Zaman from [Julia Ebert](https://juliaebert.com/).*
        </vue-markdown>
      </div>
    </div>

  </div>
</footer>
</template>

<script>
import VueMarkdown from "vue-markdown";

export default {
  components: {
    VueMarkdown
  }
};
</script>

<style lang="scss">
</style>
