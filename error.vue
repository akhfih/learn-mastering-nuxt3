<template>
  <NuxtLayout>
    <div class="prose">
      <h1>Dang</h1>
      <p>It looks like something broke</p>
      <p>
        <strong>{{ error.message }}</strong>
      </p>
      <p>
        Go to the
        <a class="hover:cursor-pointer" @click="handlerError"> first lesson </a>
      </p>
    </div>
  </NuxtLayout>
</template>

<script setup>
const error = useError();
const handlerError = () => {
  clearError({
    redirect:
      '/course/chapter/1-chapter-1/lesson/1-introduction-to-typescript-with-vue-js-3',
  });
};
</script>
