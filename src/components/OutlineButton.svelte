<script lang="ts">
	import { toTitleCase } from "../utils/toTitleCase";

	export let text = 'y0ng0p3';
	export let isCall = false;
  export let href = '/';
  $: link = text.split(' ').map(word => word.toLowerCase()).join('-');

</script>

<a href={isCall ? `https://wa.me/${text}` : href + link} class={isCall ? 'bold-900' : ''}>
	{toTitleCase(text)}
</a>

<style>
	a {
		text-decoration: none;
		border-radius: 4px;
		font-family: -apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Oxygen, Ubuntu, Cantarell,
			Open Sans, Helvetica Neue, sans-serif;
		color: #30c57a;
		padding: 8px 24px;
	}
	a:hover {
		/* background-color: #d9fde5; */
	}
	.bold-900 {
		font-weight: 900;
	}
</style>
