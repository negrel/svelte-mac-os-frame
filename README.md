![package size](https://img.shields.io/github/size/nergel3/svelte-mac-os-frame/src/index.svelte)
![npm version](https://img.shields.io/npm/v/svelte-mac-os-frame?color=green)
# svelte-mac-os-frame

> A mac os window frame svelte component.

Basic :
![](https://raw.githubusercontent.com/negrel/svelte-mac-os-frame/master/resources/frame1.jpg)

### Installation

```
npm install svelte-mac-os-frame
```

### Example

Live example [here](https://negrel.dev/svelte-fullpage.js/#page2).

##### Customized example: 

```html
<script>
	// Example of svelte-mac-os-frame component.
	// After 'npm install svelte-mac-os-frame' you can use it :
	import MacOsFrame from 'svelte-mac-os-frame';

	const title = 'svelte_logo.jpg';

	const option = {
		headerStyle: { background: "#1C1D21", color: "whitesmoke" },
		bodyStyle: {},
		titleStyle: { color: 'whitesmoke', textShadow: 'unset' },
		title
	}
</script>

<MacOsFrame {...options}>
	<img src="https://svelte.dev/svelte-logo-horizontal.svg" alt={title}>
</MacOsFrame>
```

![](https://raw.githubusercontent.com/negrel/svelte-mac-os-frame/master/resources/frame1.jpg)


### :stars: Show Your Support
Please give a :star: if this project helped you!

#### :scroll: License
MIT © Alexandre Negrel

