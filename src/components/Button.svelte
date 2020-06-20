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
</script>

<button class="lemon-btn {type} {cls}" style="border-radius: {radius ? radius: '0px'}">
	<slot></slot>
</button>

<style>
	.lemon-btn {
		padding: 1em;
		border: 0;
		cursor: pointer;
		font-size: 16px;
	}
	.lemon-btn.rounded {
		border-radius: 50%;
	}
</style>