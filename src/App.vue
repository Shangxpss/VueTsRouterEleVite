<script setup lang="ts">
type MessageOf<T extends { message: unknown }> = T["message"];

interface Email {
  message: string;
}
interface Iphone{
  a:number
}

type EmailMessageContents = MessageOf<Email>;
type EmailMessageC = MessageOf<{message:number}>;
let email:EmailMessageC = 3
console.log(email)



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
