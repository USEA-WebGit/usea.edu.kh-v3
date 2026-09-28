<template>
  <section class="relative min-h-[600px] overflow-hidden bg-[#8fa363]">
    <div class="grid min-h-[600px] grid-cols-1 lg:grid-cols-12">
      <!-- Left -->
      <div class="relative lg:col-span-4">
        <img
          :src="slides[currentSlide].image"
          :alt="slides[currentSlide].title"
          class="absolute bottom-0 left-12 w-3/4 object-contain"
        />
      </div>

      <!-- Right -->
      <div class="flex items-center lg:col-span-8">
        <div class="w-full bg-yellow-400 p-10 text-center">
          <h1 class="text-3xl font-bold">
            {{ slides[currentSlide].title }}
          </h1>

          <p class="mt-4 text-xl font-semibold">
            {{ slides[currentSlide].subtitle }}
          </p>

          <p class="mt-6">
            {{ slides[currentSlide].description }}
          </p>

          <button class="mt-8 rounded-full bg-blue-900 px-8 py-3 text-white">
            Learn More
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const currentSlide = ref(0);

const slides = [
  {
    id: 1,
    title: "Professional Graduate Certificate in Education",
    subtitle: "Elevate Your Teaching. Expand Your Horizons.",
    description: "Developed and delivered in collaboration...",
    image: "/images/hero/teacher.webp",
  },
  {
    id: 2,
    title: "Study at University of South-East Asia",
    subtitle: "Build Your Future With Us",
    description: "Explore our academic programs...",
    image: "/images/hero/teacher.webp",
  },
  {
    id: 3,
    title: "International Education",
    subtitle: "Learn Without Borders",
    description: "Discover international opportunities...",
    image: "/images/hero/teacher.webp",
  },
];

const nextSlide = () => {
  currentSlide.value++;

  if (currentSlide.value >= slides.length) {
    currentSlide.value = 0;
  }
};

const previousSlide = () => {
  currentSlide.value--;

  if (currentSlide.value < 0) {
    currentSlide.value = slides.length - 1;
  }
};
</script>
