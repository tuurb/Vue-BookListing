<template>
<div>
  <h1>{{title}}</h1>
  <ul>
    <li v-for="book in books" :key='book.id'>
      {{book.title}}: {{book.author}}
    </li>
  </ul>
</div>

</template>

<script>
export default {
  name: 'BookList',
  data() {
    return {
      title: 'All Books',
      books: [
        {id: 1, title: 'Self-Reliance', author: 'Ralph Waldo Emerson'},
        {id: 2, title: 'American Gods', author: 'Neil Gaiman'},
        {id: 3, title: 'Amusing Ourselves to Death', author: 'Neil Postman'},
      ],
    };
  },
}
</script>

<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
</style>
