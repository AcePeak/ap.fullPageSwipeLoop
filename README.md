# ap.fullPageSwipeLoop.js

Based on [fullPage](http://alvarotrigo.com/fullPage/) but make it swipes more smooth and loop-able.

## Usage
As you can see the swipeloop.html file in the example files, you will need to include:
 - [jQuery library](http://jquery.com/). (1.6.0 minimum)
 - The JavaScript file `ap.fullPageSwipeLoop.js` (or its minified version `ap.fullPageSwipeLoop.min.js`)
 - The css file `ap.fullPageSwipeLoop.css`

###Required HTML structure
In order to create a landscape loopable slider within a section, each slide will be defined with another `div`. Besides, another 2 slides should be duplicated from the original first and last slide div and seperately copied after the original last one and before the original first one. Like this:
```html
<div class="section">
	<div class="slide swipe"> Slide 4 </div>
	<div class="slide"> Slide 1 </div>
	<div class="slide"> Slide 2 </div>
	<div class="slide"> Slide 3 </div>
	<div class="slide"> Slide 4 </div>
	<div class="slide swipe"> Slide 1 </div>
</div>
````
You can see a fully working example of the HTML structure in the [`swipeloop.html` file](https://github.com/acepeak/ap.fullPageSwipeLoop/blob/master/examples/swipeloop.html).


###Initialization
All you need to do is call the plugin inside a `$(document).ready` function:

```javascript
$(document).ready(function() {
	$('#fullpage').fullpage();
});
```

A more complex initialization with all options set could look like this:
```javascript
$(document).ready(function() {
	$('#fullpage').fullpage({
		//Scrolling
		css3: true,
		scrollingSpeed: 700,
		autoScrolling: true,
		scrollBar: false,
		easing: 'easeInQuart',
		easingcss3: 'ease',
		loopBottom: false,
		loopTop: false,
		loopHorizontal: true,
		continuousHorizontal: false, 				//this is newly added for swipe loop
		continuousVertical: false,
		normalScrollElements: '#element1, .element2',
		scrollOverflow: false,
		touchSensitivity: 15,
		normalScrollElementTouchThreshold: 5,
	});
});
```
