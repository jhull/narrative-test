<template>
<div>
  <div class="max-w-2xl px-4 py-10 m-auto bg-white sm:px-8 sm:shadow dark:bg-gray-800 sm:rounded">
    <ContentDoc v-slot="{ doc }"
      class="prose prose-gray dark:prose-invert max-w-none">
      <!-- <BannerImage v-if="doc.banner_slug" :banner_slug="doc.banner_slug" class="mb-8" /> -->
      <div class="mb-8 prose prose-gray dark:prose-invert max-w-none">
        <h1>{{ doc.title }}</h1>
        <p class="-mt-6 text-gray-400">{{ doc.tldr }}</p>
      </div>
      <ContentRenderer class="prose prose-gray dark:prose-invert max-w-none" :value="doc" />
    </ContentDoc>
  </div>
  <!-- <TeamListing v-if="$route.path === '/about'" /> -->
</div>
</template>

<style lang="postcss">
/* Customize headers to remove default underline */
.prose h2 a,
.prose h3 a {
  @apply no-underline;
  &:hover {
    @apply border-b border-neutral-600 dark:border-neutral-300;
  }
}
</style>
