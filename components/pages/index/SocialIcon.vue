<template>
  <li
    class="p-2 border border-transparent rounded-full shadow-sm bg-a-black-700 focus-within:border-orchid-500"
  >
    <a
      :href="href"
      class="focus:outline-none group"
      target="_blank"
      rel="noopener"
      :title="title"
    >
      <svg
        viewBox="0 0 24 24"
        fill="none"
        stroke="currentColor"
        stroke-width="1"
        stroke-linecap="round"
        stroke-linejoin="round"
        class="w-6 h-6 text-white transition-colors group-hover:text-orchid-500 group-focus:text-orchid-500"
        :aria-label="`${title} icon`"
      >
        <slot></slot>
      </svg>
    </a>
  </li>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: () => null,
    },

    href: {
      type: String,
      default: () => null,
    },
  },
}
</script>
