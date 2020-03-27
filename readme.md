#A Simple Vue HTML Image Component With A Fixed Aspect Ratio

Use this image component when you want to display images with a fixed aspect ratio, defined by you, like: 1/1 or 16/9... or any other ratio.

The width of the image will be 100% of the parent container. The component will determine the image height, so that it will always have the given aspect ratio.

This component uses the `apl-vue-ar-container` package to set the aspect ratio.

##Install

``$ npm install apl-vue-ar-image``

or

``$ yarn add apl-vue-ar-image``

##Usage

**In a Vue file:**

```javascript
import ArImage from 'apl-vue-ar-image';

export default {
	components: {
        'ar-image': ArImage,
	},

    //...
}
```

**In a js file (like Laravel's app.js):**

```javascript
window.Vue = require('vue');

Vue.component('ar-image', require('apl-vue-ar-image').default);

const app = new Vue({
    el: '#app',
});
```

**Then in your HTML:**

```html
<ar-image ar="4/3" src="/path/to/an/image.jpg" fit="cover"></ar-image>
```

###Parameters

* **ar** - (mandatory) The aspect ratio of the image, as a string with the format: WIDTH/HEIGHT (e.g. 1/1, 16/9, 4/3 etc.)
* **src** - (mandatory) The url to the image to be displayed
* **fit** - (optional | default: cover) How to fit the image in the container with the fixed aspect ratio (options: cover, contain, fill, none, scale-down) (check CSS: `object-fit`)

###Styling

Although you can add any class to the container, there is not much that makes sense, other than a simple border. I recommend styling the parent container if you want borders with padding or other specific styling.