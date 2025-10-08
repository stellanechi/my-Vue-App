<!-- <script>
export default {
  data: () => ({
    buttonMessage: "Login User",
    user: null,
  }),
  methods: {
    loginUser() {
      this.user = {
        firstName: "Stella",
        lastName: "Eneh",
      };
    },
  },
};
</script>

<template>
  <button @click="loginUser">{{ buttonMessage }}</button>
  <div>Welcome: {{ user?.firstName }} {{ user?.lastName }}</div>
</template>

<style></style> -->

<script>
export default {
  data: () => ({
    buttonMessage: "Login User",
    isLoggedIn: false,
    user: null,
    students: [
      { name: "Franklin", age: 40 },
      { name: "David", age: 20 },
      { name: "Jessica", age: 12 },
      { name: "Yahaya", age: 14 },
      { name: "Stella", age: 18 },
      { name: "Samuel", age: 19 },
      { name: "Adamu", age: 21 },
    ],
  }),
  methods: {
    loginUser() {
      // Login Yourself
      this.user = { firstName: "Funmilayo", lastName: "Oba" };
      this.isLoggedIn = true;
    },
    logout() {
      // Login Yourself
      this.user = null;
    },
  },
  computed: {
    getFullName() {
      return this.user
        ? `${this.user.firstName} ${this.user.lastName}`
        : "No User Logged In";
    },
    getAdultStudents() {
      return this.students.filter((s) => s.age >= 18);
    },
    getLoggedInProperties() {
      return { ...this.user, isLoggedIn: this.isLoggedIn };
    },
  },
};
</script>

<template>
  <button @click="loginUser">{{ buttonMessage }}</button>
  <button @click="logout">Logout</button>
  <div>Welcome: {{ getFullName }}</div>
  <div>{{ getAdultStudents }}</div>
</template>

<style></style>

<!-- <script setup>
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <div>
    <a href="https://vite.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <HelloWorld msg="Vite + Vue" />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style> -->
