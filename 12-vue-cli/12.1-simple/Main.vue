<template>
  <div class="container">
    <div class="jumbotron">
      <h1 class="display-4" v-html="greeting"></h1>
      <p class="mvui-text-muted">{{dateString}}</p>
      <p class="lead">Lorem ipsum dolor sit amet.</p>
      <hr class="my-4">
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam, reprehenderit.</p>
      <a class="btn btn-primary btn-lg" href="#" role="button">Foobar</a>
    </div>
    <bs-alert-components/>
    <bs-button-components/>
  </div>
</template>

<script>
import BsAlertComponents from "./components/AlertComponents.vue";
import BsButtonComponents from "./components/ButtonComponents.vue";

import "./node_modules/bootstrap/dist/css/bootstrap.min.css";
import "./custom.css";

export default {
  data: function() {
    return {
      greeting: `Hello World!`,
      dateString: new Date().toLocaleString()
    };
  },
  components: {
    BsAlertComponents,
    BsButtonComponents
  }
};
</script>

<style scoped lang="scss">
$muted-color: #ccc;

.mvui-text-muted {
  color: $muted-color;
}
</style>