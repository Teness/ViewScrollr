#ViewScrollr by [Mode54](http://m54.co/home)

A Custom Titanium Scrollable View Module

##About

This module is a custom wrapper around the Ti.UI.ScrollableView object to provide extra features. The two main features are auto scrolling and custom paging controls.

Visit our [Titanium blog](http://TiHelp.me) for more code, tips & tricks. You can also checkout [Mode54.com](http://m54.co/home) for our products and services. Code Strong!

##Usage

Here is a quick example of how to use ViewScrollr

```javascript
var ViewScrollr = require("ViewScrollr");

var Banner = ViewScrollr.create({
	top        : 0,
	height     : 180,
	auto       : true,
	navigation : {
		selectedColor   : "#fff",
		color           : "#000",
		backgroundColor : "#000"
	},
	panels : [
		{ image : "/images/sunset_houses.jpg" },
		{ image : "/images/beach.jpg" },
		{ image : "/images/lizard.jpg" },
		{ image : "/images/cove.jpg" },
		{ image : "/images/bermuda.jpg" }
	]
});

win.add(Banner);
```
## Configuration

The `create()` method can take a number of parameters to customize the appearance and behavior of the ViewScrollr.

* **top, bottom, left, right** _[OPTIONAL]_ Position of ViewScrollr relative to the parent. Same as [Ti.UI.View](http://docs.appcelerator.com/titanium/latest/#!/api/Titanium.UI.View) properties.
* **width, height** _[OPTIONAL]_ Size of ViewScrollr in platform-specific units. Same as [Ti.UI.View](http://docs.appcelerator.com/titanium/latest/#!/api/Titanium.UI.View) properties. **_(default: Ti.UI.FILL)_**
* **backgroundColor** _[OPTIONAL]_ The background color of the container. If your view or image is smaller then the width or height then you will see this color in the background. **_(default: #000)_**
* **auto** _[OPTIONAL]_ Enable/Disable auto scroll feature. **_(default: false)_**
* **delay** _[OPTIONAL]_ Delay between panel auto scroll in milliseconds. **_(default: 4000)_**
* **alpha** _[OPTIONAL]_ Alpha (opacity) value of navigation background. **_(default: 0.5)_**
* **navigation** _[OPTIONAL]_ Navigation (page control) settings. Settings object is required to display navigation.
	* **onTop** _[OPTIONAL]_ Move navigation (and captions) to top of ViewScrollr
	* **style** _[OPTIONAL]_ Set navigation style. Either `ViewScrollr.NAV_STYLE.CIRCLE` or `ViewScrollr.NAV_STYLE.BLOCK` **_(default: ViewScrollr.NAV_STYLE.CIRCLE)_**
	* **selectedColor** _[REQUIRED]_ Color of the selected page indicator.
	* **color** _[REQUIRED]_ Color of page indicators.
	* **showBorder** _[OPTIONAL]_ Enable/Disable page indicator borders.
	* **borderColor** _[OPTIONAL]_ Color of page indicator borders.
	* **backgroundColor** _[OPTIONAL]_ Background color of navigation & caption. **_(default: #000)_**
* **panels** _[REQUIRED]_ Panel object settings. These are required for this module to function. I'd recommend more then one.
	* **view** _[REQUIRED]_ A Ti.UI.View object. This is only required if `image` is not set.
	* **image** _[REQUIRED]_ A string with the path/url to an image. This is only required if `view` is not set. If both exist then `image` takes priority.
	* **caption** _[OPTIONAL]_ The text to display as a caption for this panel.
	* **maxZoomScale** _[OPTIONAL]_ If this is set then the `image` is wrapped in a Ti.UI.ScrollView with this maxZoomScale. This allows zooming. (see [Ti.UI.ScrollView](http://docs.appcelerator.com/titanium/latest/#!/api/Titanium.UI.ScrollView-property-maxZoomScale))

## Video Preview

<a href="http://www.youtube.com/watch?feature=player_embedded&v=8aUx_DD2nE8" target="_blank"><img src="https://raw.github.com/Mode54/ViewScrollr/master/Resources/images/video_poster.png" alt="ViewScrollr Video Preview" width="635" height="385" border="0" /></a>

## Sources and Credits
		
I've used the following images from [kansasphoto's photostream](http://www.flickr.com/photos/34022876@N06/) on Flickr via [Creative Commons Search tool](http://search.creativecommons.org/).</p>
		
* [Beach](http://www.flickr.com/photos/34022876@N06/6873017519)
* [Bermuda HDR](http://www.flickr.com/photos/34022876@N06/7679656016)
* [Jobson's Cove](http://www.flickr.com/photos/34022876@N06/3763170877)
* [Jamaican Anole](http://www.flickr.com/photos/34022876@N06/7680071526)
* [DSC_0243_4_5](http://www.flickr.com/photos/34022876@N06/6893964117)

## ViewScrollr Pro Version

We released a pro version to this module with some cool extra features like animated content blocks and video slides. [Download it here!](http://m54.co/ViewScrollrPro)

## Got Bugs?

Log them in the [Issues section](https://github.com/Mode54/ViewScrollr/issues). Please provide details and reproducible test cases if possible.
