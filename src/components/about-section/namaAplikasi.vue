<template>
  <div class="nama-aplikasi">
    <div class="container-hero">
      <navigation-menu />
      <div class="hero py-16 px-16">
        <h1>Dolan Travel</h1>
        <p>
          Dolan Travel merupakan perusahaan asal Yogyakarta, yang memulai
          bisnisnya pada tahun 2022, dengan berfokus untuk membantu masyarakat
          menemukan perjalanan liburan terbaik.
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.nama-aplikasi {
  width: 100%;
  height: 100vh;
  background: #161616;
  position: relative;
}

.nama-aplikasi .container-hero {
  background-image: url("../../assets/bg-home-section1.png");
  position: relative;
  height: 100vh;
  display: flex;
  flex-direction: column;
  background-size: cover;
}

.nama-aplikasi .container-hero::before {
  content: "";
  width: 100%;
  height: 100%;
  background-image: linear-gradient(to bottom, rgba(255, 255, 255, 0), #000);
  position: absolute;
  bottom: 0;
}

.nama-aplikasi .hero {
  position: relative;
  height: 100%;
  z-index: 2;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.nama-aplikasi .hero p {
  color: rgba(255, 255, 255, 0.8);
  width: 600px;
  text-align: center;
}

.hero h1 {
  font-size: 140px;
  font-weight: bold;
  color: white;
  word-spacing: 8px;
  animation-name: glow;
  animation-duration: 1s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
}

@keyframes glow {
  from {
    text-shadow: 0px 0px 5px #fff, 0px 0px 5px #161616;
  }
  to {
    text-shadow: 0px 0px 15px #fff, 0px 0px 15px #161616;
  }
}

.hero h1 div {
  overflow: hidden;
  transition: 1s cubic-bezier(0.39, 0.575, 0.565, 1);
  width: fit-content;
  margin: 0 auto;
  position: relative;
  color: rgb(250, 136, 28);
  text-shadow: 0px 0px 8px rgba(250, 136, 28, 0.25);
}

.hero h1 div.hide {
  opacity: 0%;
  transform: translateY(-50%);
}

.container-partner {
  height: 30%;
  padding-top: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
  /* background: #000; */
}
</style>

<script>
import NavigationMenu from "../NavigationMenu.vue";
export default {
  name: "nama-aplikasi",
  components: { NavigationMenu },
  data() {
    return {};
  },
  methods: {},
};
</script>
