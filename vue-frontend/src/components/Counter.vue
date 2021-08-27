<template>

  <div>

<!--    <p>I'm a Counter!</p>     -->
    <p>Current count (Episodes seen) : {{ count }} </p>

    <div id="button-1">
      <button v-on:click="count += 1">Increment</button>
    </div>

    <div id="button-2">
      <button v-on:click="count -= 1">Decrement</button>
    </div>

  </div>

</template>

<script>
export default {
  
  props: {
    count: {
      default: 0,
      type: Number
    }
  },

};
</script>


<style>
#button-1 {
  margin-top: 1%;
  margin-left: 5%;
  margin-right: 5%;
}

#button-2 {
  margin-top: 1%;
  margin-left: 5%;
  margin-right: 5%;
}
</style>