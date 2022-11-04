<template>
  <div class="justify-center flex bg-gray-100 items-center h-screen">
    <div class="text-4xl hello">Hello <span> 🙌</span></div>
  </div>
</template>

<script>
import anime from "animejs/lib/anime.es.js";

export default {
  name: "HeadVue",
  mounted() {
    let text = document.querySelector(".hello");
    text.innerHTML = text.textContent.replace(
      /\S/g,
      "<span class='letters'>$&</span>"
    );

    anime.timeline({ loop: false }).add({
      targets: ".letters",
      translateX: [20, 0],
      opacity: [0, 1],
      easing: "easeOutExpo",
      delay: (el, i) => 100 * i,
    });
  },
};
</script>
