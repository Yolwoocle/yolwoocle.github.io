<script lang="ts">
	import CardGrid from '../../CardGrid.svelte';

	let projects = [
		[

		],
	];
</script>

<div class="w-full flex flex-col items-center">
	<div class="max-w-215 px-5 text-center text-(--main-very-dark)">
		<h1 class="font-black text-4xl pt-6 pb-4">Projects</h1>
		<div class="flex flex-col gap-3 text-left">
			<p class="text-xl">
				Here's a bunch of stuff that didn't fit a specific category.
			</p>
		</div>
		<CardGrid cards={projects} cardWidth="240px" cardHeight="320px" />
	</div>
</div>

<style>
	.star {
		animation: constantRotation 8s linear infinite;
        display: inline-block;
	}

	@keyframes constantRotation {
		0% {
			transform: rotate(0);
		}
		100% {
			transform: rotate(360deg);
		}
	}
</style>
