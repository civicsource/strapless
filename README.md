# Strapless
> A collection of shared variables from bootstrap and our own mixins

## Why does this exist?!?!?!

So we can `require` shared vars from bootstrap for consistent look & feel without fooling with paths to less files after an `npm dedupe`.

See [this explanation](http://caitpotter.blogspot.com/2013/08/strapless-unadulterated-twbs-without.html) by somebody who came up with a similar idea and the same package name.

## How do I use this stupid thing!!?!?!?!?!

```
npm install --save-dev @civicsource/strapless
```

Then in your app's code:

ES6 Style (preferred):

```javascript
import { bootstrap } from "@yournpmfeed/strapless";
```

browserify ES5 style:

```javascript
var bootstrap = require("@yournpmfeed/strapless").bootstrap;
```

## Example use in a react component's render method:

```javascript
import React from "react";
import { bootstrap } from "@yournpmfeed/strapless";
import Color from "color-forge";

export default class MyPrettyPony extends React.Component {
	render() {
		// the pony will run away if you get its haircut too dirty
		const maneColor = Color(bootstrap.grayLighter).mix(Color(botstrap.grayDark), (this.props.petCount / this.props.ponyPatienceThreshold);

		const ponyStyle = {
			padding: `${bootstrap.paddingBaseVertical} ${bootstrap.paddingBaseHorizontal}`,
			backgroundColor: maneColor
		};

		return (
			<div style={ponyStyle}>Be gentle</div>
		);
	}
}
```
