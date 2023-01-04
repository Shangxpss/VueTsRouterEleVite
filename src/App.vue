<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
interface Shape {
  kind: "circle" | "square";
  radius?: number;
  sideLength?: number;
}

// ---cut---
function getArea(shape: Shape) {
  if (shape.kind === "circle") {
    return Math.PI * shape.radius! ** 2;
  }
}

let a = getArea({kind:"circle",radius:3})
console.log(a)
</script>

<template>
  <header>
    <div >
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <br>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>

</style>
