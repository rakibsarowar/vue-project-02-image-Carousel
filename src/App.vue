<template>
  <h1 class="text-2xl text-center">Image Carousel</h1>
  <div class="container mx-auto p-4">
    <ImageCarousel :images="imageUrls" />
  </div>
</template>

<script>
import ImageCarousel from "./components/ImageCarousel.vue";

export default {
  components: {
    ImageCarousel,
  },
  data() {
    return {
      imageUrls: [
        "https://images.unsplash.com/photo-1672331085984-766d0104d4d1?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NXx8c3VuJTIwYXQlMjBzdW5zZXR8ZW58MHx8MHx8fDA%3D&auto=format&fit=crop&w=500&q=60",
        "https://images.unsplash.com/photo-1659645687954-52b82be586da?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Nnx8c3VuJTIwYXQlMjBzdW5zZXR8ZW58MHx8MHx8fDA%3D&auto=format&fit=crop&w=500&q=60",
        "https://images.unsplash.com/photo-1651166403368-0cd7b89a2792?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8OXx8c3VuJTIwYXQlMjBzdW5zZXR8ZW58MHx8MHx8fDA%3D&auto=format&fit=crop&w=500&q=60",
        // Add more image URLs as needed
      ],
    };
  },
};
</script>
