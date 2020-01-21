<div class="mac-os-frame">
	<div class="mac-os-frame_header">
		<div class="mac-os-frame_header_buttons">
			<div class="mac-os-frame_header_button_left" />
			<div class="mac-os-frame_header_button_middle" />
			<div class="mac-os-frame_header_button_right" />
		</div>
		<div class="mac-os-frame_header_title">
			{ title }
		</div>
	</div>
	<div class="mac-os-frame_body">
		<slot />
	</div>
</div>

<script>
// Title props
export let title = "";
</script>

<style>
.mac-os-frame {
	border-radius: .5em;
	overflow: hidden;
	box-shadow: 0 7px 8px -4px rgba(0, 0, 0, 0.2), 0 12px 17px 2px rgba(0, 0, 0, 0.14), 0 5px 22px 4px rgba(0, 0, 0, 0.12);
}

.mac-os-frame_header {
	position: relative;
	padding: .5em .75em;
	display: flex;
	justify-content: space-between;
	background: rgb(201,200,206);
	background: linear-gradient(0deg, rgba(201,200,206,1) 0%, rgba(230,229,241,1) 100%);}

.mac-os-frame_header * {
	display: inline-block
}

.mac-os-frame_header_title {
	position: absolute;
	top: 50%;
	left: 50%;
	transform: translate(-50%, -50%);
	opacity: .5;
	font-size: .75em;
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