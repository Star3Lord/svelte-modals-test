<script lang="ts">
  const year = new Date().getFullYear();
</script>

<footer>
  <div>
    <p>John Doe © {year}</p>
    <p>All Rights Reserved</p>
  </div>
</footer>

<style>
  footer {
    @apply mt-auto relative bg-gray-800;
  }

  div {
    @apply mx-auto my-8 max-w-[480px] md:mx-12 md:max-w-full text-white;
  }
</style>
