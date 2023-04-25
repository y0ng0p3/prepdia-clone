<script lang="ts">
  import { toTitleCase } from "../utils/toTitleCase";
  
	export let text = 'y0ng0p3';
	export let isCall = false;
	export let outlined = false;
  export let href = '/';
  $: link = text.split(' ').map(word => word.toLowerCase()).join('-');
</script>

<a href={isCall ? `https://wa.me/${text}` : href + link} class={outlined ? 'bold-900 bordered' : isCall ? 'bold-900' : ''}>
	<svg
		class={!isCall ? 'x-none' : ''}
		xmlns="http://www.w3.org/2000/svg"
		width="15.377"
		height="15.399"
		x="0"
		y="0"
		version="1.1"
		viewBox="0 0 15.377 15.399"
		xml:space="preserve"
		><g transform="translate(-75.078 -48.12)"
			><g transform="matrix(.27253 0 0 .29135 277.18 160.721)"
				><path
					fill="#6f758e"
					fill-opacity="1"
					stroke-width="0.107"
					d="M-686.616-347.493l-7.015-6.57c-1.933-1.812-5.08-1.812-7.014 0l-3.189 2.986c-1.465 1.373-3.849 1.372-5.313 0l-13.82-12.955c-1.469-1.376-1.469-3.602 0-4.978l3.188-2.986c1.926-1.804 1.953-4.742-.002-6.572l-7.012-6.548c-1.934-1.812-5.081-1.812-7.01-.004l-2.556 2.373c-6.974 6.532-6.974 17.161 0 23.693l21.897 20.522c6.99 6.547 18.304 6.548 25.295 0l2.55-2.39c1.935-1.811 1.935-4.759 0-6.57zm-44.854-35.433a1.736 1.736 0 012.34.002l7.013 6.548a1.48 1.48 0 010 2.19l-1.169 1.095-9.347-8.755zm19.347 42.203l-21.897-20.522c-5.396-5.054-5.693-12.99-.913-18.375l9.32 8.73c-2.449 2.6-2.347 6.562.307 9.048l13.82 12.955c2.651 2.484 6.881 2.586 9.66.289l9.32 8.73c-5.731 4.469-14.184 4.234-19.617-.855zm23.169-2.39l-1.17 1.096-9.352-8.761 1.17-1.095a1.736 1.736 0 012.337 0l7.015 6.57a1.482 1.482 0 010 2.19z"
				/></g
			></g
		></svg
	>
	{toTitleCase(text)}
</a>

<style>
	a {
		text-decoration: none;
		border-radius: 4px;
		font-family: -apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Oxygen, Ubuntu, Cantarell,
			Open Sans, Helvetica Neue, sans-serif;
		color: #6f758e;
		padding: 0 24px;
    margin-left: 16px

	}
	a:hover {
		/* background-color: #d9fde5; */
	}
	.bold-900 {
		font-weight: 900;
	}
  .bordered {
		color: #30c57a;
		border: solid 1px #30c57a;
		padding: 12px 24px;
    margin: 0;
  }
	.x-none {
		display: none !important;
	}
</style>
