<template>
  <div class="about">
    <h1>This is an about page</h1>
    <div class="table-main">
    <table class="user-table">
        <tr class="topic">
          <th>Name</th>
          <th>Phone</th>
          <th>E-mail</th>
          <th>Website</th>
        </tr>
        <tr>
          <td>
            <p v-for="user in users" :key="user.id" class="text-detail">{{user.name}}</p>
          </td>
          <td>
            <p v-for="phone in users" :key="phone.id" class="text-detail">{{phone.phone}}</p>
          </td>
          <td>
            <p v-for="email in users" :key="email.id" class="text-detail">{{email.email}}</p>
          </td>
          <td>
            <p v-for="web in users" :key="web.id" class="text-detail">{{web.website}}</p>
          </td>
        </tr>
        <!-- เขียนแบบย่อ -->
        <tr v-for="user in users" :key="user.id" >
          <td><p class="text-detail">{{ user.name }}</p></td>
          <td><p class="text-detail">{{ user.phone }}</p></td>
          <td><p class="text-detail">{{ user.email }}</p></td>
          <td><p  class="text-detail">{{ user.website }}</p></td>
        </tr>
      </table>
    </div>
  </div>
</template>

<script>
import userData from '@/store/users.json'
export default {
  data() {
    return { users: userData}
  }
}
</script>

<style>
.table-main {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.topic{
  height: 50px;
  font-size: 20px;
}
.user-table td{
  width: 250px;
  height: 50px;
  text-align: left;
}
.user-table,td,th{
  border: 1px solid;
  /* collapse ทำให้เส้นของตารางมีเส้นเดียว */
  border-collapse: collapse;
}
.text-detail {
  margin-left: 10px;
}
</style>