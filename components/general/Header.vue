<template>
  <nav x-data="{ open: false }" class="bg-gray-900 border-black border-b">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16">
        <div class="flex items-center">
          <div class="flex-shrink-0">
            <img class="h-8 w-8" src="logo.svg" alt="Workflow" />
          </div>
          <div class="hidden md:block">
            <div class="ml-10 flex items-baseline space-x-4">
              <nuxt-link to="/" class="menu-link">
                Home
              </nuxt-link>
              <nuxt-link to="/partslog" class="menu-link">
                絵巻欠片
              </nuxt-link>
            </div>
          </div>
        </div>
        <div class="hidden md:block">
          <div class="ml-4 flex items-center md:ml-6">
            <button
              class="p-0 rounded-full text-gray-400 hover:text-gray-300 focus:outline-none focus:bg-blue-800 focus:text-white"
            >
              <span class="sr-only">View Help</span>
              <svg
                class="h-7 w-7"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M8.228 9c.549-1.165 2.03-2 3.772-2 2.21 0 4 1.343 4 3 0 1.4-1.278 2.575-3.006 2.907-.542.104-.994.54-.994 1.093m0 3h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
                />
              </svg>
            </button>
          </div>
        </div>
        <div class="-mr-2 flex md:hidden">
          <!-- Mobile menu button -->
          <button
            type="button"
            class="bg-gray-900 inline-flex items-center justify-center p-2 rounded-md text-gray-500 hover:text-gray-400 hover:bg-gray-800 focus:outline-none focus:bg-gray-800"
            aria-controls="mobile-menu"
            @click="open = !open"
            aria-expanded="false"
            x-bind:aria-expanded="open.toString()"
          >
            <span class="sr-only">Open main menu</span>
            <svg
              x-state:on="Menu open"
              x-state:off="Menu closed"
              class="block h-6 w-6"
              :class="{ hidden: open, block: !open }"
              x-description="Heroicon name: outline/menu"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              aria-hidden="true"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
            </svg>
            <svg
              x-state:on="Menu open"
              x-state:off="Menu closed"
              class="h-6 w-6 block"
              :class="{ block: open, hidden: !open }"
              x-description="Heroicon name: outline/x"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              aria-hidden="true"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
            </svg>
          </button>
        </div>
      </div>
    </div>

    <div
      x-description="Mobile menu, show/hide based on menu state."
      class="md:hidden"
      id="mobile-menu"
      x-show="open"
      v-if="open"
    >
      <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
        <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
        <nuxt-link to="/" class="mobile-menu-link">Home</nuxt-link>

        <nuxt-link to="/partslog" class="mobile-menu-link">
          絵巻欠片
        </nuxt-link>
      </div>
      <div class="pt-4 pb-3 border-t border-gray-700">
        <div class="px-2 space-y-1">
          <a
            href="#"
            class="flex block px-3 py-2 rounded-md text-base text-gray-400 hover:text-white hover:bg-gray-700"
          >
            <svg
              class="h-7 w-7 mr-2"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M8.228 9c.549-1.165 2.03-2 3.772-2 2.21 0 4 1.343 4 3 0 1.4-1.278 2.575-3.006 2.907-.542.104-.994.54-.994 1.093m0 3h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
              />
            </svg>
            <div class="font-medium">
              Help
            </div>
          </a>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      open: false
    }
  }
}
</script>

<style lang="postcss" scoped>
.mobile-menu-link {
  @apply bg-gray-900 block px-3 py-2 rounded-md text-base font-medium;
}
.menu-link {
  @apply font-medium px-3 py-2 rounded-md text-sm;

  &.nuxt-link-exact-active {
    @apply bg-gray-800 text-gray-400;
  }
  &:hover {
    @apply bg-gray-800 text-gray-400;
  }
}
/*

.light-mode {
  & .nuxt-link-exact-active {
    @apply text-accent-600;
    &:hover {
      @apply text-white;
    }
  }
} */
</style>
