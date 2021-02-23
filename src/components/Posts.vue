<template>
  <div>
    <table class="table table-striped mt-4">
      <thead>
        <tr>
          <th scope="col">#</th>
          <th scope="col">User ID</th>
          <th scope="col">Title</th>
          <th scope="col">Body</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="post in posts" :key="post.id">
          <th scope="row">{{ post.id }}</th>
          <td>{{ post.userId }}</td>
          <td>{{ post.title }}</td>
          <td>{{ post.body }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "Posts",
  data() {
    return {
      posts: []
    };
  },
  created() {
    axios.get("https://jsonplaceholder.typicode.com/posts").then(posts => {
      this.posts = posts.data;
    });
  }
};
</script>

<style>
</style>
