<template>
  <div
    class="nav-menu py-4 px-16 flex justify-between items-center w-full"
    :style="[mouseScroll ? { background: 'black', padding: '8px 32px' } : '']"
  >
    <h1 class="py-4 logo text-xl font-semi">
      <router-link to="/">DolanTravel.</router-link>
    </h1>

    <ul class="flex gap-8">
      <li><router-link to="/services">Produk</router-link></li>
      <li><router-link to="/about">Tentang Kami</router-link></li>
      <li class="special">Book Now</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "navigation",
  data() {
    return { mouseScroll: 0 };
  },
  mounted() {
    window.addEventListener("scroll", () => {
      this.mouseScroll = window.scrollY;
    });
  },
};
</script>

<style scoped>
.nav-menu {
  position: absolute;
  top: 0;
  z-index: 5;
  transition: 1s ease;
}

li {
  padding: 4px 16px;
  cursor: pointer;
  transition: 1s ease;
}

li.special {
  background: #ff5a5f;
  border-radius: 20px;
  box-shadow: 0px 0px 4px #ff5a5f;
}

li.special:hover {
  animation: hoverAnim 3s ease infinite;
  transform: scale(1.1);
}

@keyframes hoverAnim {
  0% {
    box-shadow: 0px 0px 4px #ff5a5f;
  }

  25% {
    box-shadow: 0px 0px 16px #ff5a5f;
  }

  50% {
    box-shadow: 0px 0px 32px rgb(110, 30, 240);
  }

  75% {
    box-shadow: 0px 0px 16px rgb(110, 30, 240);
  }

  100% {
    box-shadow: 0px 0px 4px rgb(110, 30, 240);
  }
}
</style>
