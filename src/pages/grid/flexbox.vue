<template>
  <div class="flexbox">
    <div class="header" />
    <div class="body" />
    <div class="footer" />
  </div>
</template>

<style scoped>
.flexbox {
  height: 100%;
  display: flex;
  flex-direction: column;
  background-color: green;
}

.header {
  height: 150px;
  background-color: red;
}

.body {
  flex: 1;
  background-color: yellow;
}

.footer {
  height: 150px;
  background-color: blue;
}
</style>
