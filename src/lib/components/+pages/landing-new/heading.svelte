<script context="module" lang="ts">
	import { onMount } from 'svelte';
</script>

<script lang="ts">
	let containerNode: HTMLDivElement;

	let windowHeight: number;

	let topfadeOut = false;

	onMount(() => {
		const containerRect = containerNode.getBoundingClientRect();

		const topPos = 200;

		topfadeOut = containerRect.bottom < topPos;
	});
</script>

<svelte:document
	on:scroll={() => {
		const containerRect = containerNode.getBoundingClientRect();

		const topPos = 200;

		topfadeOut = containerRect.bottom < topPos;
	}}
/>
<svelte:window bind:innerHeight={windowHeight} />

<div bind:this={containerNode}>
	<h1
		class={`text-[2.5rem] font-light uppercase tracking-widest leading-none transition-colors ease-out duration-700 ${
			topfadeOut ? 'text-gray-6' : 'text-gray-12'
		}`}
	>
		Tech-poiesis
	</h1>

	<!-- <p class="leading-none tracking-widest mt-xxs flex font-thin text-[15px]">
		Bespoke website creation
	</p> -->

	<p class="tracking-widest mt-xs flex font-thin text-[15px] max-w-[300px]">
		<span
			class={`transition-colors ease-out duration-500 ${
				topfadeOut ? 'text-gray-6' : 'text-my-olive'
			}`}>B</span
		>
		<span
			class={`transition-colors ease-out duration-500 ${
				topfadeOut ? 'text-gray-6' : 'text-my-olive'
			}`}>e</span
		>
		<span
			class={`transition-colors ease-out duration-500 ${
				topfadeOut ? 'text-gray-6' : 'text-my-light-blue'
			}`}>s</span
		>
		<span
			class={`transition-colors ease-out duration-500 ${
				topfadeOut ? 'text-gray-6' : 'text-my-dark-red'
			}`}>p</span
		>
		<span
			class={`transition-colors ease-out duration-500 ${
				topfadeOut ? 'text-gray-6' : 'text-my-sea-green'
			}`}>o</span
		>
		<span
			class={`transition-colors ease-out duration-500 ${
				topfadeOut ? 'text-gray-6' : 'text-my-dark-olive'
			}`}>k</span
		>
		<span
			class={`mr-xxs transition-colors ease-out duration-500 ${
				topfadeOut ? 'text-gray-6' : 'text-my-orange'
			}`}>e</span
		>

		<span
			class={`transition-colors ease-out duration-500 ${
				topfadeOut ? 'text-gray-6' : 'text-my-rosy-brown '
			}`}>w</span
		>
		<span
			class={`transition-colors ease-out duration-500 ${
				topfadeOut ? 'text-gray-6' : 'text-my-dark-slate-gray '
			}`}>e</span
		>
		<span
			class={`transition-colors ease-out duration-500 ${
				topfadeOut ? 'text-gray-6' : 'text-my-plum '
			}`}>b</span
		>
		<span
			class={`transition-colors ease-out duration-500 ${
				topfadeOut ? 'text-gray-6' : 'text-my-dark-olive '
			}`}>s</span
		>
		<span
			class={`transition-colors ease-out duration-500 ${
				topfadeOut ? 'text-gray-6' : 'text-my-dark-olive '
			}`}>i</span
		>
		<span
			class={`transition-colors ease-out duration-500 ${
				topfadeOut ? 'text-gray-6' : 'text-my-steel-blue '
			}`}>t</span
		>
		<span
			class={`mr-xxs transition-colors ease-out duration-500 ${
				topfadeOut ? 'text-gray-6' : 'text-my-royal-blue '
			}`}>e</span
		>

		<span
			class={`transition-colors ease-out duration-500 ${
				topfadeOut ? 'text-gray-6' : 'text-my-golden-rod '
			}`}>c</span
		>
		<span
			class={`transition-colors ease-out duration-500 ${
				topfadeOut ? 'text-gray-6' : 'text-my-dark-olive '
			}`}>r</span
		>
		<span
			class={`transition-colors ease-out duration-500 ${
				topfadeOut ? 'text-gray-6' : 'text-my-navy-blue '
			}`}>e</span
		>
		<span
			class={`transition-colors ease-out duration-500 ${
				topfadeOut ? 'text-gray-6' : 'text-my-navy-blue '
			}`}>a</span
		>
		<span
			class={`transition-colors ease-out duration-500 ${
				topfadeOut ? 'text-gray-6' : 'text-my-plum '
			}`}>t</span
		>
		<span
			class={`transition-colors ease-out duration-500 ${
				topfadeOut ? 'text-gray-6' : 'text-my-plum '
			}`}>i</span
		>
		<span
			class={`transition-colors ease-out duration-500 ${
				topfadeOut ? 'text-gray-6' : 'text-my-dark-red '
			}`}>o</span
		>
		<span
			class={`transition-colors ease-out duration-500 ${
				topfadeOut ? 'text-gray-6' : 'text-my-golden-rod '
			}`}>n</span
		>
		<span class="ml-xs"> for individuals and small companies, hobbyists and professionals, </span>
	</p>
</div>
