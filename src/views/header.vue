<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-dark">
      <!-- <div class="toggle">
        <i class="mdi mdi-menu" @click="sidebarShow"></i>
      </div> -->
      
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarTogglerDemo02"
        aria-controls="navbarTogglerDemo02"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarTogglerDemo02">
        <ul class="navbar-nav mt-2 mt-lg-0">
          <li class="nav-item active">
            <router-link to="/" class="nav-link"><div class="navbar-brand" href="#">
        <img
          src="../assets/Untitled design (2).png"
          width="40"
          height="40"
          class="d-inline-block align-top"
          alt
        >
      </div></router-link>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#whatwedo">What We Do</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#about">About Us</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#contact">Contact Us</a>
          </li>
          <li class="nav-item">
            <router-link to="/stayupdated" class="nav-link"> Stay Updated </router-link>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#testimonial">Testimonials</a>
          </li>
          <li class="nav-item">
            <router-link to="/profile" class="nav-link">Profile</router-link>
          </li>
          <li class="nav-item">
        <login></login>
      </li>
      <li class="nav-item">
        <signup></signup>
      </li>
        </ul>
      </div>
    </nav>
  </div>
</template>

<script>
import login from "./login.vue";
import signup from "./signup.vue";

export default {
  components: {
    "login": login,
    "signup": signup
  },
  data() {
    return {};
  },
  methods: {
    sidebarShow() {
      this.$store.commit("sidebarToggle");
    }
  },
  computed: {
    image() {
      return this.$store.state.picture;
    }
  }
};
</script>

<style scoped>
ul {
  list-style-type: none;
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
}
li {
  display: inline-block;
  margin: 0 20px;
  padding: 20px;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
}
a {
  text-decoration: none;
  padding: 6px 8px;
  position: relative;
}
a:hover {
  text-decoration: none;
  background-color: rgba(223, 209, 13, 0.699);
  border-radius: 50px;
  min-width: 5vh;
}
a:active {
  color: red !important;
}
.navbar {
  background-color: orangered;
}

.navbar-toggler-icon {
  color: black;
}
.image {
  background-position: center center;
  background-repeat: no-repeat;
  background-size: contain;
  min-height: 10px;
  /* background-color: red; */
  position: absolute;
}
.navbar-brand {
  border-radius: 50%;
}
</style>
