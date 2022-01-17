<template>
  <div>
    <h1>Search</h1>
    <form @submit.prevent="submit">
      <div>
        <label for="name">Keyword</label>
        <br />
        <input
          type="text"
          v-model="keyword"
          name="keyword"
          id="keyword"
          class="form-field"
        />
      </div>
      <div>
        <input type="submit" value="Search" />
      </div>
    </form>
    <div v-for="p of photos" class="row" :key="p.id">
      <div>
        <img :src="p.photoFile" />
      </div>
      <div>{{ p.name }}</div>
      <div>{{ p.description }}</div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import { APIURL } from "../constant";

export default {
  name: "SearchPage",
  data() {
    return {
      keyword: "",
      photos: [],
    };
  },
  watch: {
    $route: {
      immediate: true,
      handler() {
        this.keyword = this.$route.query.q;
        this.search();
      },
    },
  },
};
</script>
