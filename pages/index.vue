<template>
  <section id="posts">
    <PostPreview
      v-for="post in posts"
      :key="post.id"
      :id="post.id"
      :title="post.title"
      :excerpt="post.previewText"
      :thumbnail-image="post.thumbnailUrl"
    />
  </section>
</template>

<script>
import PostPreview from '@/components/Blog/PostPreview'
export default {
  components: {
    PostPreview
  },
  data() {
    return {
      posts: [
        {
          title: 'A new beginning',
          previewText: "This will be awesome, don't miss it!",
          thumbnailUrl:
            'https://tinylaptop.net/wp-content/uploads/2016/12/best-laptop-for-programming.jpg',
          id: 'a-new-beginning'
        },
        {
          title: 'A second beginning',
          previewText: "This will be awesome, don't miss it!",
          thumbnailUrl:
            'https://tinylaptop.net/wp-content/uploads/2016/12/best-laptop-for-programming.jpg',
          id: 'a-second-beginning'
        },
        {
          title: 'A new beginning',
          previewText: "This will be awesome, don't miss it!",
          thumbnailUrl:
            'https://tinylaptop.net/wp-content/uploads/2016/12/best-laptop-for-programming.jpg',
          id: 'a-new-beginning'
        },
        {
          title: 'A second beginning',
          previewText: "This will be awesome, don't miss it!",
          thumbnailUrl:
            'https://tinylaptop.net/wp-content/uploads/2016/12/best-laptop-for-programming.jpg',
          id: 'a-second-beginning'
        },
        {
          title: 'Paleo Pizza',
          previewText: 'This will be awesome!',
          thumbnailUrl:
            'https://www.washingtonpost.com/resizer/M-WnldvRmvg3qyWg0Om8ssM6E3M=/1484x0/arc-anglerfish-washpost-prod-washpost.s3.amazonaws.com/public/UM4VXMMJ5Y7T5MPQALWPL73RGM.jpg',
          id: 'paleo-pizza'
        },
        {
          title: 'Flatbread Pizza',
          previewText: 'This will be awesome!',
          thumbnailUrl:
            'https://www.washingtonpost.com/resizer/M-WnldvRmvg3qyWg0Om8ssM6E3M=/1484x0/arc-anglerfish-washpost-prod-washpost.s3.amazonaws.com/public/UM4VXMMJ5Y7T5MPQALWPL73RGM.jpg',
          id: 'flatbread-pizza'
        }
      ]
    }
  }
}
</script>

<style scoped>
#posts {
  padding-top: 2rem;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  flex-wrap: wrap;
}

@media (min-width: 35rem) {
  #posts {
    flex-direction: row;
  }
}
</style>
