<template>
  <div class="column login-form">
    <div class="heading">Login</div>
    <hr />

    <!-- form start -->
    <div class="form">
      <div class="input-group">
        <label for="email" class="input-label">Email</label>
        <input id="email" type="text" placeholder="Enter your email" />
      </div>
      <div class="input-group">
        <span class="input-label">
          Password
        </span>
        <input type="password" placeholder="Enter your password" />
      </div>
      <div class="button-container">
        <span class="button" @click="submitForm">
          Submit
        </span>
      </div>
    </div>
    <!-- form end -->

  </div>
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

.input-label {
  display: block;
  width: 100px;
  font-weight: 500;
  margin-bottom: 10px;
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

.button {
  display: inline-block;
  background: $secondary;
  color: $white;
  font-weight: 800;
  font-size: 1.3rem;
  font-family: 'Avenir', sans-serif;
  padding: 10px 15px;

  &:hover {
    background: $third;
    color: $secondary;
    transition: all ease 0.1s;
    cursor: pointer;
  }
}

// Other styles
.login-form {
  font-size: 1.2rem;
}

hr {
  border: 1px solid tomato;
  margin-bottom: 40px;
}

.heading {
  font-size: 1.8rem;
  font-weight: 500;
  margin-bottom: 1.5rem;
  margin-top: 20px;
}
</style>
