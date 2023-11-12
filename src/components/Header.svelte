<script>
	// @ts-nocheck

	/**
	 * @typedef {Object} FlipbookHeaderProps
	 * @property {() => void} closeModal - Function to close the modal
	 */

	/** @type {FlipbookHeaderProps} */
	let { closeModal } = $props();
</script>

<div class="headerWrapper">
	<div class="left" />
	<div class="center" />
	<div class="right">
		<button on:click={closeModal}>X</button>
	</div>
</div>

<style>
	.headerWrapper {
		display: flex;
		align-items: center;
		width: 100%;
		min-height: 2rem;
		background-color: #4d5356;
		padding: 1rem 0;
		gap: 0.5rem;
	}

	.left {
		width: 25%;
	}

	.center {
		width: 50%;
	}

	.right {
		width: 25%;
		display: flex;
		justify-content: flex-end;
	}
	button {
		background-color: transparent;
		border: none;
		color: white;
		font-size: 1.2rem;
		margin-right: 0.5rem;
	}
</style>
