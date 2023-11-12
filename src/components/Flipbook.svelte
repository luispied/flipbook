<script>
	import FlipbookHeader from './Header.svelte';

	/**
	 * @typedef {Object} FlipbookProps
	 * @property {() => void} closeModal - Function to close the modal
	 */

	/** @type {FlipbookProps} */
	let { closeModal } = $props();
</script>

<div class="flipbookContainer">
	<div class="flipbookWrapper">
		<FlipbookHeader {closeModal} />
		<h1>Flipbook</h1>
	</div>
</div>

<style>
	.flipbookContainer {
		display: flex;
		flex-direction: column;
		min-width: 800px;
		min-height: 600px;
	}
	.flipbookWrapper {
		display: flex;
		flex-direction: column;
		flex: 1 1 0;
		align-items: center;
	}
</style>
