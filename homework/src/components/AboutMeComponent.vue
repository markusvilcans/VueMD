<script>
export default {
  data() {
    return {
      user: {
        name: "Markus",
        surname: "Vilcans",
        code: "IT20003",
      },
    };
  },
};
</script>

<template>
  <h1>ABOUT ME</h1>
  <h3>Vārds: {{ user.name }}</h3>
  <h3>Uzvārds: {{ user.surname }}</h3>
  <h3>Kods: {{ user.code }}</h3>
</template>

<style></style>
