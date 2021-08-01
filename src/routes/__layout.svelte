<script>
  import { browser } from '$app/env';
  import { Modals, closeModal } from 'svelte-modals';
  import Footer from '$lib/components/Footer.svelte';
  import '../app.css';

  if (browser) {
    if (
      localStorage.theme === 'dark' ||
      (!('theme' in localStorage) &&
        window.matchMedia('(prefers-color-scheme: dark)').matches)
    ) {
      document.documentElement.classList.add('dark');
    } else {
      document.documentElement.classList.remove('dark');
    }
  }
</script>

<div class="min-h-screen relative flex flex-col dark:bg-black">
  <slot />

  <!-- <Footer /> -->
</div>

<Modals>
  <div
    slot="backdrop"
    class="backdrop"
    on:click={closeModal}
  />
</Modals>

<style>
  .backdrop {
    position: fixed;
    top: 0;
    bottom: 0;
    right: 0;
    left: 0;
    background: rgba(0,0,0,0.50)
  }
</style>
