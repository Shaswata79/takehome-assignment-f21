<template>
  <div>
    <!-- PART 1: Pass in a "complete" prop here -->
    <Instructions 
      v-bind:complete="true"
    />
    <!-- PART 4: Modify the Show component to accept all of these props -->
    <Show
      v-for="show in shows"
      :key="show.id"
      :id="show.id"
      :name="show.name"
      :episodes_seen="show.episodes_seen"
    />

    <div id="add_show">
      <p> Add a Show </p>
      <input v-model="showName" placeholder="New show name">
      <button v-on:click="addShow">Add new show</button>
    </div>

  </div>
</template>



<script>
import Instructions from "./Instructions.vue";
import Show from "./Show.vue";

export default {
  components: {
    Instructions,
    Show
  },
  data() {
    return {
      shows: [
        { id: 1, name: "Game of Thrones", episodes_seen: 0 },
        { id: 2, name: "Naruto", episodes_seen: 220 },
        { id: 3, name: "Black Mirror", episodes_seen: 3 }
      ],
      lastId: 3, 
      showName: "",
    };
  },

  methods: {
    addShow(){
      var new_id = this.lastId + 1;
      this.shows.push({id: new_id, name: this.showName, episodes_seen: 0});
      this.showName = "";
    }
  }


};
</script>




<style>
  #add_show {
    margin-top: 10%;
    margin-left: 5%;
    margin-right: 5%;
    margin-bottom: 10%;
  }
</style>


