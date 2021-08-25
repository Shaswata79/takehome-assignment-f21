<template>
  <!-- PART 4: Add your code here -->
  <div id="show_details">
    <p>
      Show name: {{name}}    <Counter v-bind:count="episodes_seen"/>
    </p>

  </div>
</template>



<script>
  import Counter from "./Counter.vue";
// PART 4: Add your code here
  export default {
    components: {
      Counter
    },
    props: {'id':"",
      'name':"",
      'episodes_seen':0 },
  };
</script>



<style>
  #show_details {
  margin-top: 5%;
  margin-left: 5%;
  margin-right: 5%;
}
</style>
