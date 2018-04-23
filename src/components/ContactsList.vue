<template>
  <div>
    
    <form @submit.prevent="addContact">

      <label>First Name</label>
      <input v-model="newContact.firstName" type="text" placeholder="First Name"/>

      <label>Last Name</label>
      <input v-model="newContact.lastName" type="text" placeholder="Last Name"/>

      <label>Email</label>
      <input v-model="newContact.email" type="email" placeholder="Email"/>

      <button type="submit">Add Contact</button>

    </form>



    <table>
      <thead>
        <th>First Name</th>
        <th>Last Name</th>
        <th>Email</th>
      </thead>

      <tbody>
        <tr v-for="(contact, key) in contacts" :key="key">
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
      
      ],

      newContact: {
        firstName: '',
        lastName: '',
        email: ''
      }
    }
  },
  methods: {
    addContact() {
      this.contacts.push(this.newContact)
      this.newContact = {}
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
