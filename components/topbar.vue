<template>
  <div class="topbar-container">
    <div class="topbar-img-container">
      <img class="topbar-img color-burn">
    </div>
    <div class="form-control">
      <input type="value" required="">
      <label>
        <span style="transition-delay:0ms">S</span><span style="transition-delay:50ms">e</span><span
          style="transition-delay:100ms">a</span><span style="transition-delay:150ms">r</span><span
          style="transition-delay:200ms">c</span><span style="transition-delay:250ms">h</span>
      </label>
    </div>
    <label class="notifications-container">
      <input type="checkbox" checked="checked">
      <svg class="bell-regular" xmlns="http://www.w3.org/2000/svg" height="1em" viewBox="0 0 448 512">
        <path
          d="M224 0c-17.7 0-32 14.3-32 32V49.9C119.5 61.4 64 124.2 64 200v33.4c0 45.4-15.5 89.5-43.8 124.9L5.3 377c-5.8 7.2-6.9 17.1-2.9 25.4S14.8 416 24 416H424c9.2 0 17.6-5.3 21.6-13.6s2.9-18.2-2.9-25.4l-14.9-18.6C399.5 322.9 384 278.8 384 233.4V200c0-75.8-55.5-138.6-128-150.1V32c0-17.7-14.3-32-32-32zm0 96h8c57.4 0 104 46.6 104 104v33.4c0 47.9 13.9 94.6 39.7 134.6H72.3C98.1 328 112 281.3 112 233.4V200c0-57.4 46.6-104 104-104h8zm64 352H224 160c0 17 6.7 33.3 18.7 45.3s28.3 18.7 45.3 18.7s33.3-6.7 45.3-18.7s18.7-28.3 18.7-45.3z">
        </path>
      </svg>
      <svg class="bell-solid" xmlns="http://www.w3.org/2000/svg" height="1em" viewBox="0 0 448 512">
        <path
          d="M224 0c-17.7 0-32 14.3-32 32V51.2C119 66 64 130.6 64 208v18.8c0 47-17.3 92.4-48.5 127.6l-7.4 8.3c-8.4 9.4-10.4 22.9-5.3 34.4S19.4 416 32 416H416c12.6 0 24-7.4 29.2-18.9s3.1-25-5.3-34.4l-7.4-8.3C401.3 319.2 384 273.9 384 226.8V208c0-77.4-55-142-128-156.8V32c0-17.7-14.3-32-32-32zm45.3 493.3c12-12 18.7-28.3 18.7-45.3H224 160c0 17 6.7 33.3 18.7 45.3s28.3 18.7 45.3 18.7s33.3-6.7 45.3-18.7z">
        </path>
      </svg></label>

    <label class="hamburger">
      <input type="checkbox" />
      <svg viewBox="0 0 32 32">
        <path
          d="M27 10 13 10C10.8 10 9 8.2 9 6 9 3.5 10.8 2 13 2 15.2 2 17 3.8 17 6L17 26C17 28.2 18.8 30 21 30 23.2 30 25 28.2 25 26 25 23.8 23.2 22 21 22L7 22"
          class="line line-top-bottom"></path>
        <path d="M7 16 27 16" class="line"></path>
      </svg>
    </label>
  </div>
</template>

<script setup>
import { ref, watch } from 'vue';
const showNotifications = ref(false);
const showDropdown = ref(false);
const userImage = ref('user.png');
const search = () => {
  // Implement search functionality
};
const toggleNotifications = () => {
  showNotifications.value = !showNotifications.value;
};
const toggleDropdown = () => {
  showDropdown.value = !showDropdown.value;
};
watch(() => showDropdown.value, (value) => {
  if (!value) {
    showNotifications.value = false;
  }
});
// Add CSS styles and media queries to customize the topbar layout and behavior


</script>

<style></style>