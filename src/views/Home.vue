<template>
  <div class="home">
  <h1>home</h1>
  <PostList :posts="posts" />
  </div>
</template>

<script>
import PostList from '../components/PostList.vue'
import { ref } from 'vue'

export default {
  name: 'Home',
  components: {PostList},
  setup() {
    const posts = ref([
      {title: 'welcome to the blog', body: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Voluptatem fugiat vitae, et, modi, officiis ipsum alias magnam soluta animi quos laborum corrupti! Ab sunt esse at dignissimos laborum recusandae quaerat tempore, qui modi nam temporibus corrupti suscipit et expedita blanditiis quod, perferendis animi itaque harum delectus. Ipsa id, minus repellat rerum non doloremque laboriosam fugit amet enim deserunt quae sit cumque, ut omnis quisquam nihil, vel tempore praesentium est consequuntur corrupti consectetur tenetur excepturi. Minima, accusamus! Porro, laudantium excepturi. Deleniti, quia. Nam voluptatum enim assumenda vero obcaecati necessitatibus eaque ad consequatur dignissimos! Voluptatum, laboriosam vitae reprehenderit consectetur quasi odio magni.' , id: 1},
      {title: 'top 5 ninja tools', body: 'Lorem ipsum', id: 2}
    ])

    return {posts}
  }
}
</script>
