<script lang="ts">
	import FlatButton from './FlatButton.svelte';
</script>

<header>
	<h1 class="x-left">
    <a href="/">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
        width="141.889"
        height="21.86"
        viewBox="0 0 141.889 21.86"
      >
        <image
          width="141.889"
          height="21.86"
          preserveAspectRatio="none"
          xlink:href="data:image/png;base64,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 1KsnVb5xlgAAAABJRU5ErkJggg=="
        />
      </svg>
    </a>
	</h1>
	<div class="x-right">
		<FlatButton isCall={true} text={'698964258'} />
		<FlatButton text={'login'} />
		<FlatButton text={'become a tutor'} outlined={true} />
	</div>
</header>

<style>
	header {
		/* background: #f7f7f7; */
		padding: 12px;
    display: flex;
    align-items: center;
    justify-content: space-between;
	}
	h1 {
		margin: 0;
		text-align: center;
		max-width: 10%
	}
</style>
