<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <form action="post">
      <label for="title">Termék neve</label><label for="price">Ár</label><label for="quantity">Mennyiség</label>
      <br>
      <input type="text" name="title" id="title">
      <input type="number" name="price" id="price">
      <input type="number" name="quantity" id="quantity">
      <input type="submit" value="Beküldés">
    </form>
    
    
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
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
