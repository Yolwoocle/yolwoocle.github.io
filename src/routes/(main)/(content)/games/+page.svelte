<script lang="ts">
	import CardGrid from '../../CardGrid.svelte';
	import projects from './games.json';
</script>

<div class="w-full flex flex-col items-center">
	<div class="max-w-215 px-1 text-center text-(--main-very-dark)">
		<h1 class="font-black text-4xl pt-6 pb-4">Games</h1>
		<div class="flex flex-col px-4 gap-3 text-left">
			<p class="text-xl">
				Making games has always been a part of my life. When I was little, 
				I started with doodling levels in sketchbooks and using Scratch to make my own little games.
			</p>
			<p class="text-xl">
				Now, I have made dozens of games and co-founded a game dev band, <a class="card-link" href="https://ninesliced.com/">Ninesliced</a>, with some friends. 
				I believe that this medium is unique in its interactivty and ability to create emotions in people.  
			</p>
			<p class="text-xl">
				Projects I am particularily proud of have a
				<span>
					<img
					src="/assets/icons/star_outlined.png"
					alt="star"
					class="star w-8 relative"
					/>
				</span> attached.<br>
			</p>
			<p class="text-xl">
				You can find most projects on my <a class="card-link" href="https://yolwoocle.itch.io/">itch.io</a>.
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
