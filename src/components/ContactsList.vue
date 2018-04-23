<template>
  <div>
    <table>
      <thead>
        <th>First Name</th>
        <th>Last Name</th>
        <th>Email</th>
      </thead>

      <tbody>
        <tr v-for="(contact, key) in contacts" :key="key" 
        v-if="contact.firstName === 'Jack'">
        <td>{{ contact.firstName }}</td>
        <td>{{ contact.lastName }}</td>
        <td>{{ contact.email }}</td>
      </tr>
      </tbody>
    </table>
  </div>
</template>




<script>
export default {
  data() {
    return {
      contacts: [
        { firstName: 'Johnnie', lastName: 'Walker', email: 'johnniewalker@gmail.com'},

        { firstName: 'Jack', lastName: 'Daniels', email: 'jackdaniels@gmail.com'},
        
        { firstName: 'Aleksandar', lastName: 'Ljiljak', email: 'aleksandarljiljak@gmail.com'}
      
      ]
    }
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
