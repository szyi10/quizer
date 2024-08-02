<script lang="ts">
import { defineComponent } from "vue"

export default defineComponent({
  data() {
    return {
      colors: [
        "#dc2626",
        "#fb923c",
        "#22c55e",
        "#06b6d4",
        "#1d4ed8",
        "#6d28d9",
        "#c026d3",
      ],
    }
  },
  computed: {
    randomColor() {
      const length = this.colors.length
      const randomHEX = Math.floor(Math.random() * length)

      return this.colors[randomHEX]
    },
  },
})
</script>

<template>
  <div
    class="w-full h-svh flex flex-col items-center justify-center"
    :style="{ background: randomColor }"
  >
    <img src="/logo-banner.png" alt="Logo" />
    <button class="button-54" role="button">PLAY</button>
  </div>
</template>

<style scoped>
.button-54 {
  font-size: 24px;
  letter-spacing: 3px;
  font-weight: bold;
  text-decoration: none;
  text-transform: uppercase;
  color: #000;
  background: #fff;
  cursor: pointer;
  border: 3px solid;
  padding: 0.25em 0.5em;
  box-shadow: 1px 1px 0px 0px, 2px 2px 0px 0px, 3px 3px 0px 0px, 4px 4px 0px 0px,
    5px 5px 0px 0px;
  position: relative;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
}

.button-54:hover {
  background: #eee;
}

.button-54:active {
  box-shadow: 0px 0px 0px 0px;
  top: 5px;
  left: 5px;
}

@media (min-width: 768px) {
  .button-54 {
    padding: 0.25em 0.75em;
  }
}
</style>
