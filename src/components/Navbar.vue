<template>
  <div class="navbar">
    <div class="title">
      <strong><span class="orange">Dev</span>challenges.io</strong>
    </div>
    <ul class="nav">
      <li class="item"><a href="#">Colors</a></li>
      <li class="item"><a href="#">Typography</a></li>
      <li class="item"><a href="#">Spaces</a></li>
      <li class="item active"><a href="#">Buttons</a></li>
      <li class="item"><a href="#">Inputs</a></li>
      <li class="item"><a href="#">Grid</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  
}
</script>

<style scoped>
.navbar {
  height: 100vh;
  width: 250px;
  background: #FAFBFD;
  overflow: auto;
}

.title {
  margin: 30px 0;
  text-align: center;
}

.nav {
  list-style: none;
  margin: 80px 0;
  padding: 20px 10px;
}

.nav .item a {
  font-weight: 600;
  display: block;
  margin: 10px 0;
  padding: 10px 50px;
  color: #9E9E9E;
  text-decoration: none;
}

.nav .item.active a{
  color: #090F31;
}

.orange {
  color: #F7542E;
}
</style>