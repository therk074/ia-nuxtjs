<template>
  <div>
    <b-table :fields="fields" :items="items"></b-table>
  </div>
</template>
<script>
export default {
  data() {
    return {
      fields: [
          {
            key: 'Id',
            sortable: true
          },
          {
            key: 'userId',
            sortable: true
          },
          {
            key: 'title', 
            sortable: true,
          },
          {
            key: 'body', 
            sortable: true,
          }
        ],
    };
  },
  async asyncData({ $axios }) {
    const items = await $axios.$get(
      "https://jsonplaceholder.typicode.com/posts"
    );
    return { items };
  },

  methods: {},
};
</script>