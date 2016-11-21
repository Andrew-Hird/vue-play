<template>
  <div class="hello">
    <!-- <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <ul>
      <li><a href="https://vuejs.org" target="_blank">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank">Forum</a></li>
      <li><a href="https://gitter.im/vuejs/vue" target="_blank">Gitter Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank">Twitter</a></li>
      <br>
      <li><a href="http://vuejs-templates.github.io/webpack/" target="_blank">Docs for This Template</a></li>
    </ul>
    <h2>Ecosystem</h2>
    <ul>
      <li><a href="http://router.vuejs.org/" target="_blank">vue-router</a></li>
      <li><a href="http://vuex.vuejs.org/" target="_blank">vuex</a></li>
      <li><a href="http://vue-loader.vuejs.org/" target="_blank">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank">awesome-vue</a></li>
    </ul> -->
    <!-- <p>{{ name }} is <strong>{{ status }}</strong>.</p> -->

    <div id="my_view">
      <label for="person">person:</label>
      <input type="text" v-model="name" id="name" name="name" />
      <p>{{ name }} is {{ age }} years old and is {{ status | capitalize }}.</p>
      <h2>Friends:</h2>
      <ul>
        <li v-for="friend in friends"> {{ friend.name }}</li>
      </ul>
    </div>
    <div>
      Show items containing:
     <input v-model="search" type="text" />
     <ul>
       <!-- <li v-for="friend in friends | filterBy search in 'name'"> {{ friend.name }} </li> -->
     </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      message: 'hello',
      name: 'Cushla',
      age: 23,
      status: 'awesome',
      friends: [
        { name: 'Clyde', age: 21 },
        { name: 'Georgina', age: 20 },
        { name: 'Caitlin', age: 29 }
      ]

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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

p {
  font-size: 3em;
}
</style>
