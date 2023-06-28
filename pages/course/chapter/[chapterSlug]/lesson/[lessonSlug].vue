<template>
  <h2>Lesson</h2>
  <p>This is a lesson</p>
  <p>Chapter slug : {{ chapter.title }}</p>
  <p>Chapter slug : {{ lesson.title }}</p>
</template>

<script setup>
const course = useCourse();
const route = useRoute();

const chapter = computed(() => {
  return course.chapters.find(
    (chapter) => chapter.slug === route.params.chapterSlug
  );
});

const lesson = computed(() => {
  return chapter.value.lessons.find(
    (lesson) => lesson.slug === route.params.lessonSlug
  );
});
</script>
