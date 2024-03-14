<template>
  <div class="sidenav" :style="{ width: isOpen ? '400px' : '0' }">
    <a href="javascript:void(0)" class="closebtn" @click="closeNav">&times;</a>
    <div>
      <p style="color: green">Call In</p>
      <p style="color: white">064-5485929</p>
      <div>
        <button @click="openNav">Recipe</button>
        <button @click="">Cancel</button>
      </div>
    </div>
  </div>
  <div class="sidenav" :style="{ width: isOpen2 ? '400px' : '0' }">
    <a href="javascript:void(0)" class="closebtn" @click="closeNav2">&times;</a>
    <div>
      <p style="color: green">10:12</p>
      <p style="color: white">064-5485929</p>
      <div>
        <button @click="Hangup">Hangup</button>
      </div>
    </div>
  </div>
  <div>
    <h2>Call In Table</h2>
    <nuxt-link to="/">Call Out</nuxt-link>
    <table>
      <tr>
        <th>ID</th>
        <th>Phone</th>
        <th>Log Time</th>
        <th>Action</th>
      </tr>
      <tr>
        <td>001</td>
        <td>064-123-5678</td>
        <td>{{ new Date() }}</td>
        <td>
          <button @click="openNav">Call In</button>
          <button @click="openNav2">Call Still</button>
        </td>
      </tr>
    </table>
  </div>
</template>
<script setup>
import { ref } from "vue";

const isOpen = ref(false);
const isOpen2 = ref(false);

const openNav = () => {
  isOpen.value = true;
  document.body.style.backgroundColor = "rgba(0, 0, 0, 0.4)";
};

const closeNav = () => {
  isOpen.value = false;
  document.body.style.backgroundColor = "white";
};

const openNav2 = () => {
  isOpen2.value = true;
  document.body.style.backgroundColor = "rgba(0, 0, 0, 0.4)";
};

const closeNav2 = () => {
  isOpen2.value = false;
  document.body.style.backgroundColor = "white";
};
</script>
<style lang="css">
table {
  font-family: arial, sans-serif;
  border-collapse: collapse;
  width: 100%;
}

td,
th {
  border: 1px solid #dddddd;
  text-align: left;
  padding: 8px;
}

tr:nth-child(even) {
  background-color: #dddddd;
}

body {
  font-family: "Lato", sans-serif;
  transition: background-color 0.5s;
}

.sidenav {
  height: 100%;
  width: 0;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 0;
  background-color: #111;
  overflow-x: hidden;
  transition: 0.5s;
  padding-top: 60px;
}

.sidenav a {
  padding: 8px 8px 8px 32px;
  text-decoration: none;
  font-size: 25px;
  color: #818181;
  display: block;
  transition: 0.3s;
}

.sidenav a:hover {
  color: #f1f1f1;
}

.sidenav .closebtn {
  position: absolute;
  top: 0;
  right: 25px;
  font-size: 36px;
  margin-left: 50px;
}

#main {
  transition: margin-left 0.5s;
  padding: 16px;
}

@media screen and (max-height: 450px) {
  .sidenav {
    padding-top: 15px;
  }
  .sidenav a {
    font-size: 18px;
  }
}
</style>
