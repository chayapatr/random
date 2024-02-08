<script lang="ts">
	let choice = [''];
	let rand = '';
</script>

<div class="flex flex-col justify-center gap-2 p-4">
	{#each choice as i}
		<input type="text" name="" bind:value={i} id="" class="w-full rounded-md border-2 px-2 py-1" />
	{/each}
	<div class="flex gap-2">
		<button
			class="w-full rounded-md bg-neutral-600 px-2 py-1 text-white"
			on:click={() => {
				choice = [...choice, ''];
			}}>+</button
		>
		<button
			class="w-full rounded-md bg-neutral-600 px-2 py-1 text-white"
			on:click={() => {
				rand = choice[Math.floor(Math.random() * choice.length)];
			}}>🎲</button
		>
	</div>
	<div class="items-cejter flex justify-center">
		<div class={`w-min rounded-md bg-neutral-900 text-white ${rand === '' ? undefined : 'p-2'}`}>
			{rand}
		</div>
	</div>
</div>
