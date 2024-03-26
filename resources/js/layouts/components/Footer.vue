<template>
  <div class="h-100 d-flex align-center justify-space-between">
    <!-- 👉 Footer: left content -->
    <span class="d-flex align-center">
      &copy;
      {{ new Date().getFullYear() }}
      Made With
      <VIcon
        icon="tabler-heart"
        color="error"
        size="1.25rem"
        class="mx-1"
      />
      By <a
        href="#"
        target="_blank"
        rel="noopener noreferrer"
        class="text-primary ms-1"
      >Hiccup Solutions</a>
    </span>
    <!-- 👉 Footer: right content -->
    <span class="d-md-flex gap-x-4 text-primary d-none">
      <a
        href="#"
        target="noopener noreferrer"
      >Cookies</a>
      <a
        href="#"
        target="noopener noreferrer"
      >Terms & Condition</a>
      <a
        href="#"
        target="noopener noreferrer"
      >Privacy Policy</a>
      <a
        href="#"
        target="noopener noreferrer"
      >Support</a>
    </span>
  </div>
</template>
