## vizceral-svelte

[![npm](https://img.shields.io/npm/v/vizceral-svelte)](https://www.npmjs.com/package/vizceral-svelte) ![GitHub](https://img.shields.io/github/license/dgzlopes/vizceral-svelte) [![Demo](https://img.shields.io/badge/live-demo-9cf)](https://vizceral-svelte-example.surge.sh/)

![](https://raw.githubusercontent.com/Netflix/vizceral/master/logo.png)

> **This project is under active development.**

This is a svelte wrapper around [Vizceral](https://github.com/Netflix/vizceral), a component for displaying traffic data on a WebGL canvas.

Inspired by [vizceral-react](https://github.com/Netflix/vizceral-react) and [vizceral-vue](https://github.com/manico/vizceral-vue).

## Installation
```bash
# npm
npm install -D vizceral-svelte
```
## Usage

```html
<script>
  import Vizceral from "vizceral-svelte";
  import traffic from "./sample_data.json";
</script>

<Vizceral {traffic}/>
```

## Options

You can control the behavior of Vizceral effect by passing specific props to the component.

#### filters

```js
// Default: []
filters: Array;
```

Array of filter definitions and current values to filter out nodes and connections. Refer to
[github.com/Netflix/Vizceral/wiki/Configuration#filters](https://github.com/Netflix/Vizceral/wiki/Configuration#filters)

#### modes

```js
modes: Object;
```

Map of modes to mode type, e.g. { detailedNode: 'volume' }

#### styles

```js
// Default: {}
styles: Object;
```

Styles to override default properties.

#### traffic

```js
// Default: {}
traffic: Object;
```

The traffic data. See [github.com/Netflix/Vizceral/wiki/How-to-Use#graph-data-format](https://github.com/Netflix/Vizceral/wiki/How-to-Use#graph-data-format) for specification.
