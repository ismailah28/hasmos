<template>
  <div class="fixed bg-white top-0 overflow-hidden w-full shadow-sm">
    <header class="mx-4 md:mx-20 sm:flex sm:align-center sm:justify-between">
      <div class="flex align-center justify-between">
        <a href="#" class="relative py-4 flex font-black text-xl tracking-tight"
          >Isma<span
            class="absolute top-4 left-11 block text-blue-500 animate-bounce"
            >'</span
          >&nbsp;il <span class="text-blue-500">[Hassan]</span>
        </a>
        <button
          type="button"
          class="transition-all block sm:hidden text-gray-500 hover:text-black focus:text-black focus:outline-none"
          @click="isOpen = !isOpen"
        >
          <svg class="h-6 w-6 fill-current" viewBox="0 0 24 24">
            <path
              v-if="isOpen"
              fill-rule="evenodd"
              d="M18.278 16.864a1 1 0 0 1-1.414 1.414l-4.829-4.828-4.828 4.828a1 1 0 0 1-1.414-1.414l4.828-4.829-4.828-4.828a1 1 0 0 1 1.414-1.414l4.829 4.828 4.828-4.828a1 1 0 1 1 1.414 1.414l-4.828 4.829 4.828 4.828z"
            />
            <path
              v-if="!isOpen"
              fill-rule="evenodd"
              d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"
            />
          </svg>
        </button>
      </div>
      <nav
        class="sm:flex flex-col sm:flex-row align-center justify-center text-center"
        :class="isOpen ? 'block' : 'hidden'"
      >
        <a
          v-for="(link, ind) of links"
          :key="ind"
          href="#"
          class="-mx-4 sm:mx-0 sm:ml-6 py-4 block transition duration-500 ease-in-out hover:opacity-50 border-b sm:border-none"
          >{{ link }}</a
        >
      </nav>
    </header>
  </div>
</template>

<script>
export default {
  data() {
    return {
      links: ['About Me', 'Experience', 'Work', 'Blog', 'Contact'],
      isOpen: false,
    }
  },
}
</script>
