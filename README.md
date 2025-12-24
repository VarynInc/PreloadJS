# PreloadJS

PreloadJS is a library to make working with asset preloading easier. It provides a consistent API for loading different
file types, automatic detection of XHR (XMLHttpRequest) availability with a fallback to tag-base loading, composite
progress events, and a plugin model to assist with preloading in other libraries such as [SoundJS](http://www.createjs.com/soundjs/).

## Example

```javascript
var queue = new createjs.LoadQueue(false);
queue.on("fileload", handleFileComplete);
queue.loadFile('http://createjs.com/assets/images/png/createjs-badge-dark.png');
function handleFileComplete(event) {
	document.body.appendChild(event.result);
}
```

## Support and Resources
* Find examples and more information at the [PreloadJS web site](http://www.preloadjs.com/)
* Read the [documentation](http://createjs.com/docs/preloadjs/)
* Discuss, share projects, and interact with other users on [reddit](http://www.reddit.com/r/createjs/).
* Ask technical questions on [Stack Overflow](http://stackoverflow.com/questions/tagged/preloadjs).
* File verified bugs or formal feature requests using Issues on [GitHub](https://github.com/createjs/PreloadJS/issues).
* Have a look at the included [examples](https://github.com/CreateJS/PreloadJS/tree/master/examples) and
[API documentation](http://createjs.com/docs/preloadjs/) for more in-depth information.

Built by [gskinner.com](http://www.gskinner.com), and is released for free under the MIT license, which means you can
use it for almost any purpose (including commercial projects). We appreciate credit where possible, but it is not a requirement.


## Classes

**LoadQueue**
The main class that manages all preloading. Instantiate a LoadQueue instance, load a file or manifest, and track
progress and complete events. Check out the [docs](http://createjs.com/docs/preloadjs/) for more information.

## Build the library

All source code is in the `./src` folder. After updating any source code, run the tests to verify your changes. See [`./tests/README.md`](./tests/README.md). If you add new code, please add a test case to validate your new code. In order to run the tests you need to run the `build next` process as the tests are run against the `preloadjs-NEXT.js` library.

Do not edit the library files in `./lib` directly, these files are generated from the `./src` folder by the build process. To build this library, see [`./build/README.md`](./build/README.md).
