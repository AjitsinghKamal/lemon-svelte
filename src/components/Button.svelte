<script>
	export const TYPE = {
		DEFAULT: 'default',
		LINK: 'link',
		GHOST: 'ghost',
		OUTLINE: 'outline',
	}
	export let type = TYPE.DEFAULT;
	export let radius = '5px';
	export let cls = '';
	export let href = null;
</script>

{#if href}
<a class="lemon-btn link" {type} {cls} href="{href}">
	<slot></slot>
</a>
{:else}
<button class="lemon-btn {type} {cls}" style="border-radius: {radius ? radius: '0px'}">
	<slot></slot>
</button>
{/if}

<style>
	.lemon-btn {
		padding: 1em;
		border: 0;
		cursor: pointer;
		font-size: 16px;
	}
	.lemon-btn.link {
		display: inline-block;
		text-decoration: none;
		color: inherit;
	}
</style>