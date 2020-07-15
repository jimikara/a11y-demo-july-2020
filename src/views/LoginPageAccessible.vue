<template>
  <main class="column login-form">
    <h1 class="heading">Login</h1>
    <hr />

    <!-- form start -->
    <form>
      <div class="input-group">
        <label for="email">Email</label>
        <input id="email" type="text" placeholder="Enter your email" />
      </div>
      <div class="input-group">
        <label for="password" class="input-label">
          Password
        </label>
        <input
          id="password"
          type="password"
          placeholder="Enter your password"
        />
      </div>
      <div class="button-container">
        <button @click="submitForm">
          Submit
        </button>
      </div>
    </form>
    <!-- form end -->

  </main>
</template>

<script>
export default {
  name: 'LoginPage',
  methods: {
    submitForm() {
      alert('form submitted 👍')
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../styles/variables';

// Form styles
.form {
  text-align: left;
}

.input-group {
  margin-bottom: 30px;
}

label {
  display: block;
  width: 100px;
  font-weight: 500;
  margin-bottom: 10px;
  text-align: left;
}

input {
  &[type='text'],
  &[type='password'] {
    min-width: 280px;
    border: 2px solid #bbb;
    background-image: none;
    background-color: transparent;
    -webkit-box-shadow: none;
    -moz-box-shadow: none;
    box-shadow: none;
    padding: 6px 8px;

    &:focus {
      outline: teal solid 2px;
    }
  }
}

.button-container {
  text-align: right;
}

button {
  display: inline-block;
  background: $secondary;
  color: $white;
  font-weight: 800;
  font-size: 1.3rem;
  font-family: 'Avenir', Helvetica, sans-serif;
  padding: 10px 15px;
  border: none;
  border-bottom: 2px solid #ccc;

  &:hover {
    background: $third;
    color: $secondary;
    transition: all ease 0.1s;
    cursor: pointer;
  }

  &:focus {
    outline: teal solid 2px;
    border-bottom: 2px solid $secondary;
  }
}

// Other styles
.login-form {
  font-size: 1.2rem;
}

hr {
  border: 1px solid darkorange;
  margin-bottom: 40px;
}

.heading {
  font-size: 1.8rem;
  font-weight: 500;
  margin-bottom: 1.5rem;
}
</style>
