<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Persons</h2>
    <ul>
      <li v-for="user in users" v-bind:key="user.id">
        {{ user.firstname }}
        {{ user.lastname }}
      </li>
    </ul>
    <!-- <p>{{ input_val }}</p> -->
    <div>
      Input Value:<input type="text" v-model="input_val">
    </div>
    <hr>
    <div>
      <button class="btn btn-primary" @click="counter++">You've clicked this button {{ counter }} times!</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      msg: 'Welcome to Your Vue.js App',
      users: [
        { id: '01', firstname: 'Sebastian', lastname: 'Stan' },
        { id: '02', firstname: 'Bill', lastname: 'Nightly' },
        { id: '03', firstname: 'Alexx', lastname: 'Hunter' }
      ],
      input_val: 'Two Way Binding',
      counter: 0
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
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
