<template>
  <div class="hello">
    <CreativeNavigation
      :navigationList="navigationList"
      :linkClick="linkClick"
    />
  </div>
</template>

<script>
import CreativeNavigation from './CreativeNavigation.vue';
export default {
  name: 'HelloWorld',
  components: {
    CreativeNavigation,
  },
  props: {
    msg: String,
  },
  methods: {
    linkClick: (e) => {
      alert('link clicked ', e);
    },
  },
  data() {
    return {
      navigationList: [
        {
          title: 'Installed CLI Plugins',
          links: [
            {
              label: 'babel',
              url: 'https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel',
            },
            {
              label: 'eslint',
              url: 'https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint',
            },
          ],
        },
        {
          title: 'Essential Links',
          links: [
            {
              label: 'Core Docs',
              url: 'https://vuejs.org',
            },
            {
              label: 'Forum',
              url: 'https://forum.vuejs.org',
            },
            {
              label: 'Community Chat',
              url: 'https://chat.vuejs.org',
            },
            {
              label: 'Twitter',
              url: 'https://twitter.com/vuejs',
            },
            {
              label: 'News',
              url: 'https://news.vuejs.org',
            },
          ],
        },
        {
          title: 'Ecosystem',
          links: [
            { label: 'vue-router', url: 'https://router.vuejs.org' },
            { label: 'vuex', url: 'https://vuex.vuejs.org' },
            {
              label: 'vue-devtools',
              url: 'https://github.com/vuejs/vue-devtools#vue-devtools',
            },
            { label: 'vue-loader', url: 'https://vue-loader.vuejs.org' },
            {
              label: 'awesome-vue',
              url: 'https://github.com/vuejs/awesome-vue',
            },
          ],
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
