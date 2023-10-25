<template>
  <footer class="footer">
    Copyright © {{ thisYear }}
    <i
      v-if="author"
      class="icon-user"
    />
    {{ author }}
    <br>
    Generated with
    <a
      href="https://vuepress.vuejs.org/"
      rel="noopener"
      target="_blank"
    >VuePress</a>
    | Theme
    <a
      href="https://github.com/ventusoon/vuepress-theme-simple"
      rel="noopener"
      target="_blank"
    >Simple</a>
  </footer>
</template>

<script>
export default {
  computed: {
    thisYear() {
      return new Date().getFullYear();
    },
    author() {
      return this.$themeConfig.author || '';
    },
  }
}
</script>
