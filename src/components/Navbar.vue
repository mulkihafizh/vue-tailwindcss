<template>
  <nav
    class="flex fixed justify-between items-center h-16 bg-white text-black w-full shadow-sm font-mono"
    role="navigation"
  >
    <div class="pl-8">
      <a class="p-2" href="#">Assalamualaikum</a>
    </div>
    <div class="px-4 cursor-pointer md:hidden" @click="open = !open">
      <svg
        class="w-6 h-6"
        fill="none"
        stroke-linecap="round"
        stroke-linejoin="round"
        stroke-width="2"
        viewBox="0 0 24 24"
        stroke="currentColor"
      >
        <path v-if="!open" d="M4 6h16M4 12h16M4 18h16"></path>
        <path v-else d="M6 18L18 6M6 6l12 12"></path>
      </svg>
    </div>
    <div class="pr-8 md:block hidden">
      <a class="p-4" href="">Home</a>
      <a class="p-4" href="#">About</a>
      <a class="p-4" href="#">Contact</a>
    </div>
  </nav>
</template>

<script>
export default {
  name: "NavbarVue",
  data() {
    return {
      open: false,
    };
  },
};
</script>
