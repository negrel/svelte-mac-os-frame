<div class="mac-os-frame">
	<div class="mac-os-frame_header" bind:this={header}>
		<div class="mac-os-frame_header_buttons">
			<div class="mac-os-frame_header_button_left" />
			<div class="mac-os-frame_header_button_middle" />
			<div class="mac-os-frame_header_button_right" />
		</div>
		<div class="mac-os-frame_header_title" bind:this={headerText}>
			{ title }
		</div>
	</div>
	<div class="mac-os-frame_body" bind:this={body}>
		<slot />
	</div>
</div>

<script>
import { onMount } from 'svelte';

// Header text props
export let title = "";

// Background color props
export let headerStyle = '',
	titleStyle = '',
	bodyStyle = '';

let header,
	headerText,
	body;

// $: header.style = headerStyle || {};
// $: body.style = bodyStyle || {};

onMount(() => {
	Object.assign(header.style, headerStyle);
	Object.assign(headerText.style, titleStyle);
	Object.assign(body.style, bodyStyle);
});


</script>

<style>
.mac-os-frame {
	position: relative;
	border-radius: .5em;
	overflow: hidden;
	box-shadow: 0 7px 8px -4px rgba(0, 0, 0, 0.2), 0 12px 17px 2px rgba(0, 0, 0, 0.14), 0 5px 22px 4px rgba(0, 0, 0, 0.12);
	width: fit-content;
	height: fit-content;
	overflow: auto;
	font-size: 16px;
}

.mac-os-frame_header {
	position: relative;
	display: flex;
	padding: .5em .75em;
	justify-content: space-between;
	background: rgb(201,200,206);
	background: linear-gradient(0deg, rgba(201,200,206,1) 0%, rgba(230,229,241,1) 100%);
}

.mac-os-frame_header * {
	display: inline-block
}

.mac-os-frame_header_title {
	position: absolute;
	top: 50%;
	left: 50%;
	transform: translate(-50%, -50%);
	font-size: .65rem;
	text-shadow: whitesmoke 0px 1px 0px;
	color: black;
}

.mac-os-frame_header_buttons > * {
	width: .75em;
	height: .75em;
	margin: 0 .25em;
	border-radius: 100%;
}

.mac-os-frame_header_buttons > .mac-os-frame_header_button_left {
	background-color: red;
}

.mac-os-frame_header_buttons > .mac-os-frame_header_button_middle {
	background-color: orange;
}

.mac-os-frame_header_buttons > .mac-os-frame_header_button_right {
	background-color: #78bb65;
}

.mac-os-frame_body {
	background-color: white;
}
</style>