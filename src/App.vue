<template>
<div class="container">
  <div class="row">
    <div class="col-xs-12">
      <br>
        <button class="btn btn-primary" @click="selectedComponents = 'appBlue'">Load the blue template</button>
        <button class="btn btn-success" @click="selectedComponents = 'appGreen'">Load green template</button>
        <button class="btn btn-danger" @click="selectedComponents = 'appRed'">Load red template</button>
        <hr>
        <component :is="selectedComponents">
          <p>this is the component</p>
        </component>
        <!-- <app-blue>
          <p>this is the component</p>
        </app-blue>
        <app-green>
          <p>this is the component</p>
        </app-green>
        <app-red>
           <p>this is the component</p>
        </app-red> -->
    </div>
  </div>
</div>
</template>

<script>
import Blue from './components/Blue.vue';
import Green from './components/Green.vue';
import Red from './components/Red.vue';

export default {
  data: function () {
    return {
      selectedComponents: "appBlue"
    }
  },
  components: {
    appBlue: Blue,
    appGreen: Green,
    appRed: Red
  }
}
</script>

<style>

</style>
