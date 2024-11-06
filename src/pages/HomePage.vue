<script setup>

</script>

<template>
  <div class="hero-bg container-fluid">
    <div class="row">
      <div class="col-8 align-items-center">
        <h1 class="hero-text">FullStack-Developer</h1>
      </div>
      <div class="col-4">
        <img src="/img/MeNoBg.png" alt="Elijah SasserCollins" class="me">
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.hero-bg {
  background-color: black;
  height: 100vh;
}

.hero-text {
  color: var(--bs-primary);
}

.me {
  width: 100%;
  object-fit: cover;
  object-position: center;
  border-radius: 2%;
}
</style>
