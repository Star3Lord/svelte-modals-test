<script>
  import { openModal } from 'svelte-modals'
  import Modal from '$lib/components/modals/Test.svelte';

  function handleClick() {
    openModal(Modal, { title: 'Alert', message: 'This is an alert' })
  }
</script>

<button on:click="{handleClick}">Open Modal</button>
