<template>
  <div id="app">
    <HelloWorld msg="Vegyes raktár"/>
    <table>
      <tr>
        <th>Termék</th>
        <th>Ár</th>
        <th>Mennyiség</th>
        <th>Operations</th>
      </tr>
      <tr v-for="row in rows" :key="row">
          <td>{{ row.title }}</td>
          <td>{{ row.price }}</td>
          <td>{{ row.quantity }}</td>
          <td>
            <input type="button" v-on:click="deleteItem(row)" value="X">
            <input type="button" value="Edit">
          </td>
      </tr>
    </table>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data() {
    return {
      rows: [
        {
          title: 'Kerék',
          price: 100,
          quantity: 12
        },
        {
          title: 'Teleszkóp',
          price: 1000,
          quantity: 300
        },
        {
          title: 'Kormány',
          price: 230,
          quantity: 5
        },
        {
          title: 'Ajtó',
          price: 45120,
          quantity: 321
        },
      ]
    }
  },
   methods : {
                deleteItem (row){
                    this.rows = this.rows.filter(function(item)
                    {
                      return row.title!=item.title
                    }
                     
                    )
                    
                    
                }
            }
 
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
table,td, th  {  
  border: 2px solid rgb(0, 0, 0);
  text-align: center;
}
table {
  border-collapse: collapse;
  width: 40%;

}
th, td {
  padding: 15px;
}
</style>
