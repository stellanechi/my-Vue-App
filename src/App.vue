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

<!-- <script>
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

<style></style> -->

<script>
export default {
  data: () => ({
    count: 0,
  }),

  methods: {
    increment() {
      this.count++;
    },
    decrement() {
      if (this.count > 0) {
        this.count--;
      }
    },
    reset() {
      this.count = 0;
    },
  },

  computed: {
    counterMessage() {
      if (this.count > 0) return `Count is positive: ${this.count}`;
      if (this.count < 0) return `Count is negative: ${this.count}`;
      return `Count is zero`;
    },
  },
};
</script>

<template>
  <div class="counter-container">
    <div class="counter-content">
      <h2>Simple Counter App</h2>
      <h3>{{ counterMessage }}</h3>
      <div class="buttons">
        <button @click="decrement">-</button>
        <span>{{ count }}</span>
        <button @click="increment">+</button>
      </div>
      <button class="reset" @click="reset">Reset</button>
    </div>
  </div>
</template>

<style>
.counter-container {
  text-align: center;
  padding: 20px;
  border: 2px solid #ddd;
  border-radius: 10px;
  width: 500px;
  margin: 50px auto;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  background-color: #1abc9c;
}
.counter-content h2 {
  margin-bottom: 10px;
  color: #333;
  font-size: 3rempx;
}
.counter-content h3 {
  margin-bottom: 20px;
  color: #555;
}

.buttons {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 18px;
  margin: 10px 0;
}

button {
  background-color: white;
  color: #1abc9c;
  border: none;
  padding: 8px 20px;
  border-radius: 6px;
  cursor: pointer;
  font-size: 22px;
}

button:hover {
  background-color: #bff1e7;
}

reset {
  margin-top: 15px;
}
</style>
