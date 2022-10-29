<script>
import AboutMeComponent from "./AboutMeComponent.vue";
import HomeComponent from "./HomeComponent.vue";

export default {
  components: {
    AboutMeComponent,
    HomeComponent,
  },
  data() {
    return {
      showAbout: true,
      isActive: true,
      isActiveTwo: false,
    };
  },
  methods: {
    toggle() {
      this.isActiveTwo = false;
      this.isActive = true;
      this.showAbout = true;
    },
    toggletwo() {
      this.isActiveTwo = true;
      this.isActive = false;
      this.showAbout = false;
    },
  },
};
</script>

<template>
  <div class="row">
    <div id="left" class="column">
      <div>
        <button :class="[isActive ? 'toggled-on' : 'toggled-off']" @click="toggle">
          Home
        </button>
      </div>

      <div>
        <button :class="[isActiveTwo ? 'toggled-on' : 'toggled-off']" @click="toggletwo">
          About me
        </button>
      </div>
    </div>
    <div id="right" class="column">
      <div v-if="showAbout"><HomeComponent /></div>
      <div v-else><AboutMeComponent /></div>
    </div>
  </div>
</template>

<style>
.toggled-on {
  background-color: rgb(126, 73, 93);
}
.toggled-off {
  background-color: rgb(54, 31, 40);
}

body {
  background: rgb(54, 31, 40);
}
.row {
  display: flex;
}
#right .column {
  width: 50px;
  height: auto;
  display: flex;
}
#left {
  float: left;
  width: 120px;
  padding: 10px;
}
#right {
  float: left;
  width: auto;
  padding: 10px;
}

.row {
  background-color: rgb(54, 31, 40);
}
button {
  background-color: rgb(54, 31, 40);
  margin-bottom: 10px;
  font-size: 25px;
  margin-top: 0px;
  font-family: monospace;
}
h1,
h3 {
  margin-top: 0px;
  font-family: monospace;
}
</style>
