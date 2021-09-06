<script>
	import { tweened } from 'svelte/motion';
	import { cubicOut } from 'svelte/easing';

	const progress = tweened(0, {
		duration: 400,
		easing: cubicOut
	});
</script>

<progress class="progress" value={$progress} max="1">{$progress}</progress>

<div class="buttons has-addons">
<button class="button" on:click="{() => progress.set(0)}">
	0%
</button>

<button class="button" on:click="{() => progress.set(0.25)}">
	25%
</button>

<button class="button" on:click="{() => progress.set(0.5)}">
	50%
</button>

<button class="button" on:click="{() => progress.set(0.75)}">
	75%
</button>

<button class="button" on:click="{() => progress.set(1)}">
	100%
</button>
</div>
<style>
	progress {
		display: block;
		width: 100%;
	}
</style>