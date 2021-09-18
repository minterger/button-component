<template>
  <Navbar />
  <div class="container">
    <div class="title">Buttons</div>

    <div>
      <div class="card">
        <span class="etiqueta">&lt;Button /&gt;</span>
        <Button />
      </div>
      <div class="card">
        <span class="hover">&:hover, &:focus</span>
        <Button active />
      </div>
    </div>

    <div>
      <div class="card">
        <span class="etiqueta">&lt;Button variant="outline" /&gt;</span>
        <Button variant="outline" />
      </div>
      <div class="card">
        <span class="hover">&:hover, &:focus</span>
        <Button variant="outline" active />
      </div>
    </div>

    <div>
      <div class="card">
        <span class="etiqueta">&lt;Button variant="text" /&gt;</span>
        <Button variant="text" />
      </div>
      <div class="card">
        <span class="hover">&:hover, &:focus</span>
        <Button variant="text" active />
      </div>
    </div>

    <div>
      <div class="card">
        <span class="etiqueta">&lt;Button disableShadow /&gt;</span>
        <Button disableShadow />
      </div>
    </div>

    <div>
      <div class="card">
        <span class="etiqueta">&lt;Button disabled /&gt;</span>
        <Button disabled />
      </div>
      <div class="card">
        <span class="etiqueta">&lt;Button variant="outline" disabled /&gt;</span>
        <Button variant="outline" disabled />
      </div>
      <div class="card">
        <span class="etiqueta">&lt;Button variant="text" disabled /&gt;</span>
        <Button variant="text" disabled />
      </div>
    </div>

    <div>
      <div class="card">
        <span class="etiqueta">&lt;Button active /&gt;</span>
        <Button active />
      </div>
      <div class="card">
        <span class="etiqueta">&lt;Button variant="outline" active /&gt;</span>
        <Button variant="outline" active />
      </div>
      <div class="card">
        <span class="etiqueta">&lt;Button variant="text" active /&gt;</span>
        <Button variant="text" active />
      </div>
    </div>

    <div>
      <div class="card">
        <span class="etiqueta">&lt;Button startIcon="add_shopping_cart" /&gt;</span>
        <Button startIcon="add_shopping_cart" />
      </div>
      <div class="card">
        <span class="etiqueta">&lt;Button endIcon="add_shopping_cart" /&gt;</span>
        <Button endIcon="add_shopping_cart" />
      </div>
    </div>

    <div>
      <div class="card">
        <span class="etiqueta">&lt;Button size="sm" /&gt;</span>
        <Button size="sm" />
      </div>
      <div class="card">
        <span class="etiqueta">&lt;Button size="md" /&gt;</span>
        <Button size="md" />
      </div>
      <div class="card">
        <span class="etiqueta">&lt;Button size="lg" /&gt;</span>
        <Button size="lg" />
      </div>
    </div>

    <div>
      <div class="card">
        <span class="etiqueta">&lt;Button color="default" /&gt;</span>
        <Button color="default" />
      </div>
      <div class="card">
        <span class="etiqueta">&lt;Button color="primary" /&gt;</span>
        <Button color="primary" />
      </div>
      <div class="card">
        <span class="etiqueta">&lt;Button color="secondary" /&gt;</span>
        <Button color="secondary" />
      </div>
      <div class="card">
        <span class="etiqueta">&lt;Button color="danger" /&gt;</span>
        <Button color="danger" />
      </div>
    </div>

    <div>
      <div class="card">
        <span class="hover">&:hover, &:focus</span>
        <Button color="default" active/>
      </div>
      <div class="card">
        <span class="hover">&:hover, &:focus</span>
        <Button color="primary" active/>
      </div>
      <div class="card">
        <span class="hover">&:hover, &:focus</span>
        <Button color="secondary" active/>
      </div>
      <div class="card">
        <span class="hover">&:hover, &:focus</span>
        <Button color="danger" active/>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Button from "@/components/Button.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Button,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
#app {
  /* font-family: Avenir, Helvetica, Arial, sans-serif; */
  font-family: "Open Sans", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: flex;
}

.container {
  width: calc(100vw - 300px);
  height: 100vh;
  padding-left: 50px;
  overflow: auto;
}

.container .title {
  margin-top: 50px;
  color: #4f4f4f;
  font-size: 24px;
  font-weight: 600;
}

.container .card {
  min-width: 220px;
  padding-right: 40px;
  display: inline-block;
  margin-top: 35px;
}

.card .etiqueta {
  color: #333333;
  margin-bottom: 10px;
  display: block;
  font-size: 14px;
}

.card .hover {
  color: #828282;
  margin-bottom: 10px;
  display: block;
  font-size: 14px;
}
</style>
