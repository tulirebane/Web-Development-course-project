<template>
  <body>
    <div class="login-page">
        <div id="login-container">
          <div>
          <h3>Welcome to postIt!</h3>
          </div>
            <div>
                <h4>
                    <router-link to="/register" >Create an Account</router-link>
                </h4>
            </div>

          <div>
            <h4>Or</h4>
          </div>
          <div>
            <h3>Please Log In</h3>
            <form action="index.vue" method="post">
              <div>
                <input required type="text" name="email" placeholder="Email">
              </div>
              <div>
                <input required type="password" name="password"  placeholder="Password">
              </div>
              <div>
                <router-link to="/browse" tag="button">Log In</router-link>
              </div>
              <div>
                <small>
                  <a href="#">Forgot password?</a>
                </small>
              </div>
            </form>
          </div>
        </div>
    </div>
  </body>
</template>

<script>

    export default {
        name: 'Login',
        data() {
            return {
                input: {
                    email: "",
                    password: ""
                }
            }
        },
        methods: {}
    }
</script>
<style scoped>
* {
  font-family: 'Roboto Slab', serif;
  outline: none;
}

html, body {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
}

body {
  background-color: #0277bd;
  color: #263238;
}

a {
  color: #40c4ff;
}

      .login-page {
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
      }

    #login-container {
      background-image: url("../assets/logo1.png");
      background-size: 20% auto;
      background-repeat: no-repeat;
      background-position: 15px 15px;
      min-width: 25%;
      padding: 45px 45px;
      background-color: #ffffff;
      box-shadow: 0 0 15px rgba(38, 50, 56, 0.33);
      text-align: center;

    }

#login-container form div > input {
  padding: 8px 16px;
  margin: 4px 0;
}

    button {
        padding: 8px 16px;
        margin: 4px 0;
        color: #ffffff;
        background-color: #01579b;
        border: none;
        border-radius: 4px;
    }

button:hover {
  box-shadow: 0 0 5px rgba(38, 50, 56, 0.7);
  cursor: pointer;
}

</style>