<template>
  <div class="relative">
    <div class="overflow-hidden rounded-lg shadow-lg">
      <img
        :src="images[currentImageIndex]"
        :alt="`Image ${currentImageIndex + 1}`"
        class="w-full h-64 object-cover"
      />
    </div>
    <div class="flex justify-between mt-2">
      <button @click="prevImage" class="px-4 py-2 bg-gray-500 text-white rounded">
        Previous
      </button>
      <button @click="nextImage" class="px-4 py-2 bg-gray-500 text-white rounded">
        Next
      </button>
    </div>
  </div>
</template>

<script>
import { reactive, computed } from "vue";

export default {
  props: {
    images: {
      type: Array,
      required: true,
    },
  },
  setup(props) {
    const state = reactive({
      currentImageIndex: 0,
    });

    const nextImage = () => {
      state.currentImageIndex =
        (state.currentImageIndex + 1) % props.images.length;
    };

    const prevImage = () => {
      state.currentImageIndex =
        (state.currentImageIndex - 1 + props.images.length) % props.images.length;
    };

    return {
      currentImageIndex: computed(() => state.currentImageIndex),
      nextImage,
      prevImage,
    };
  },
};
</script>
