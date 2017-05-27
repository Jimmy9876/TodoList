<template>
  <div class="hello">
    <h1 v-text="title"></h1>
      <ul>
        <li v-for="item in items" v-bind:class="{finished: item.isFinished}">
          {{ item.label }}
        </li>
      </ul>
  </div>
</template>

<script>
export default {
  data () {
    return {
      title: 'This is a todolist.',
      items: [
        {
          label: 'coding',
          isFinished: false
        },
        {
          label: 'walking',
          isFinished: true
        }
      ],
      liClass: 'ThisisliClass'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.finished{
  text-decoration: underline;
}
h1, h2 {
  font-weight: normal;
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
