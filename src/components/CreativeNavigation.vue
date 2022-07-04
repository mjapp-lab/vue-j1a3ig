<template>
  <div class="creativeNavigation" v-for="nav in navigationList">
    <h3>{{ nav.title }}</h3>
    <ul>
      <li v-for="link in nav.links">
        <a
          href="{{link.url}}"
          @click="linkClick('test')"
          target="_blank"
          rel="noopener"
          >{{ link.label }}</a
        >
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'CreativeNavigation',
  props: {
    navigationList: Array,
    linkClick: Function,
  },
};
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
