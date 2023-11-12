<script>
	// @ts-nocheck

	import Flipbook from './Flipbook.svelte';

	/**
	 * @type {HTMLDialogElement | null}
	 */
	let dialog = $state(null);

	$effect(() => {
		dialog = document.querySelector('dialog');
	});

	function showModal() {
		dialog?.showModal();
	}

	function closeModal() {
		dialog?.close();
	}
</script>

<dialog>
	<Flipbook {closeModal} />
</dialog>

<button on:click={showModal}>Open Modal</button>

<style>
	::backdrop {
		/* background-image: linear-gradient(45deg, magenta, rebeccapurple, dodgerblue, green); */
		opacity: 0.75;
	}
	dialog {
		border: 12px solid #4d5356;
		padding: 0;
		border-radius: 8px;
	}
</style>
