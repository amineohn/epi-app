<template>
  <nav :class="{ 'is-transformed': !showNavbar }" class="navbar is-transparent">
    <div class="navbar-brand">
      <p
        class="navbar-item"
        style="background-color: transparent !important; font-size: 1.3em"
      >
        <span class="logo">Epihelpcie</span>
      </p>
      <a
        :aria-expanded="isActive"
        :class="{ 'is-active': isActive }"
        role="button"
        class="navbar-burger"
        aria-label="menu"
        data-target="collapse"
        @click="isActive = !isActive"
      >
        <span></span>
        <span></span>
        <span></span>
      </a>
    </div>

    <div
      class="navbar-menu is-paddingless"
      :class="{ 'is-active': isActive }"
      id="collapse"
    >
      <div class="navbar-start">
        <p class="navbar-item">
          <router-link to="/" class="menu-px"
            >&nbsp; Qui sommes nous ?</router-link
          >
        </p>
        <p class="navbar-item">
          <router-link to="/projet" class="menu-px-2">
           &nbsp;&nbsp;Notre projet&nbsp;</router-link
          >
        </p>
        <p class="navbar-item">
          <a
            href="https://instagram.com/epihelpcie"
            target="_blank"
            class="map"
          >
            <Instagram style="margin-bottom: -2% !important" />
            &nbsp;@epihelpcie</a
          >
        </p>
        <p class="navbar-item">
          <a href="mailto:epihelpcie@gmail.com" class="map">
            <Mail style="margin-bottom: -2% !important" />
            &nbsp;epihelpcie@gmail.com</a
          >
        </p>
      </div>
    </div>
  </nav>
</template>

<script>
import throttle from "lodash/throttle";
import Instagram from "./icons/Instagram";
import Mail from "./icons/Mail";
export default {
  components: {
    Instagram,
    Mail
  },
  data() {
    return {
      isActive: false,
      showNavbar: true,
      lastScrollPosition: 0,
    };
  },
  mounted() {
    this.$nextTick(() => {
      window.addEventListener("resize", throttle(this.closeMenu, 500));
      window.addEventListener("scroll", throttle(this.hideNav, 250));
    });
  },
  beforeDestroy() {
    window.removeEventListener("resize", this.closeMenu);
    window.removeEventListener("scroll", this.hideNav);
  },
  methods: {
    closeMenu() {
      this.isActive = false;
    },
    hideNav() {
      const currentScrollPosition =
        window.pageYOffset || document.documentElement.scrollTop;
      if (currentScrollPosition < 0) return;
      if (Math.abs(currentScrollPosition - this.lastScrollPosition) < 60)
        return;
      this.showNavbar = currentScrollPosition < this.lastScrollPosition;
      this.lastScrollPosition = currentScrollPosition;
      setTimeout(this.closeMenu, 250);
    },
  },
};
</script>

<style>
select:hover {
  transition: all 0.4s ease-out;
}
</style>