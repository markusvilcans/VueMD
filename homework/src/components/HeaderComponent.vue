<script>
export default {
  data() {
    return {
      Login: false,
      Teksts: "Login",
      user: {
        name: "Markus",
        surname: "Vilcans",
        code: "IT20003",
      },
    };
  },
  methods: {
    switcher() {
      this.Login = !this.Login;
      this.Teksts = this.Login ? "Logout" : "Login";
    },
    returnFullName() {
      return `${this.user.name} ${this.user.surname}`;
    },
  },
};
</script>

<template>
  <header>
    <div>
      <div id="header-left">
        <img
          alt="Bilde nez kapec neiet"
          src="https://ichef.bbci.co.uk/news/976/cpsprodpb/16620/production/_91408619_55df76d5-2245-41c1-8031-07a4da3f313f.jpg"
        />
      </div>

      <div id="header-right">
        <button v-on:click="switcher">{{ Teksts }}</button>
        <img
          v-if="Login"
          src="https://i.pinimg.com/originals/97/e4/2a/97e42a82fc7911961d3ca55f54d1372c.jpg"
        />
        <h3 v-if="Login">{{ returnFullName() }}</h3>
      </div>
    </div>
  </header>
</template>

<style scoped>
header {
  background-color: rgb(126, 73, 93);
  padding: 10px;
  padding-bottom: 50px;
  margin-bottom: 10px;
}
#header-left {
  float: left;
}
#header-right h3 {
  float: right;
  font-size: 25px;
  font-family: monospace;
  margin-right: 20px;
  margin-top: 5px;
  font-weight: normal;
}
#header-right button {
  float: right;
  background-color: rgb(126, 73, 93);
  font-size: 25px;
  font-family: monospace;
}
#header-left img {
  width: 40px;
  height: 40px;
}
#header-right img {
  float: right;
  border-radius: 50%;
  width: 40px;
  height: 40px;
  margin-right: 20px;
  background-color: aqua;
}
</style>
