<template>
  <div>
    <header>
      <nav>
        <div>
          <NuxtLink to="/">Home</NuxtLink> &nbsp;
          <NuxtLink to="/incrementdecrement">Increment/Decrement</NuxtLink> &nbsp;
          <NuxtLink to="/shoppinglist">Shopping List</NuxtLink>
        </div>
        <br><br>
      </nav>
    </header>

    <main>
      <NuxtPage />
    </main>

    <footer>

    </footer>
  </div>
</template>

<script setup>
  //Global app logic
</script>

<style>
  /*Global app styles */
</style>