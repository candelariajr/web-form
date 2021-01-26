<template>
  <form action="">
    <label for="email">Email:</label>
    <input id="email" type="email" required v-model="email">
    <label for="password">Password:</label>
    <input id="password" type="password" required v-model="password">
    <label for="role">Role:</label>
    <select id="role" v-model="role">
      <option value="designer">Web Designer</option>
      <option value="developer">Web Developer</option>
    </select>
    <div class="terms">
      <label for="accept">Accept terms and conditions</label>
      <input id="accept" type="checkbox" v-model="terms" required>
    </div>

    <div>
      <label for="names-Shaun">Shaun</label>
      <input id="names-Shaun" type="checkbox" value="Shaun" v-model="names">
    </div>
    <div>
      <label for="names-Yoshi">Yoshi</label>
      <input id="names-Yoshi" type="checkbox" value="Yoshi" v-model="names">
    </div>
    <div>
      <label for="names-Mario">Mario</label>
      <input id="names-Mario" type="checkbox" value="Mario" v-model="names">
    </div>
  </form>
  <p>Email: {{email}}</p>
  <p>Password: {{password}}</p>
  <p>Role: {{role}}</p>
  <p>Terms: {{terms}}</p>
  <p>Names: {{names}}</p>
</template>

<script>
export default {
  name: "SignupForm",
  data(){
    return{
      email: 'person@email.com',
      password: '',
      role: 'designer',
      terms: false,
      names: []
    }
  }
}
</script>

<style>
form{
  max-width: 420px;
  margin: 30px auto;
  background: white;
  text-align: left;
  padding: 40px;
  border-radius: 10px;
}

label{
  color: #aaa;
  display: inline-block;
  margin: 25px 0 15px;
  font-size: 0.6em;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: bold;
}

input, select{
  display: block;
  padding: 10px 6px;
  width: 100%;
  box-sizing: border-box;
  border: none;
  border-bottom: 1px solid #ddd;
  color: #555;
}

input[type="checkbox"]{
  display: inline-block;
  width: 32px;
  margin: 0 10px 0 0 ;
  position: relative;
  top: 2px;
}
</style>