mooMasonry
===========

mooMasonry is a layout plugin for Mootools. Think of it as the flip side of CSS floats. Whereas floating arranges elements horizontally then vertically, mooMasonry arranges elements vertically then horizontally according to a grid. The result minimizes vertical gaps between elements of varying height, just like a mason fitting stones in a wall.

![Screenshot](http://github.com/orefalo/mooMasonry/raw/master/Logo.png)

Comparison Example
------------------

CSS Floats
![Screenshot](https://github.com/orefalo/mooMasonry/raw/master/screen1.png)

mooMasonry
![Screenshot](https://github.com/orefalo/mooMasonry/raw/master/screen2.png)

How to use
----------

HTML code:

	<div id="primary">
    	<div class="box col2">...</div>
    	<div class="box col1">...</div>
    	<div class="box col1">...</div>
    	<div class="box col3">...</div>
    	<div>
        	<div class="box col1">...</div>
        	<div class="box col2">...</div>
        	<div class="box col3">...</div>
    	</div>
	</div>

JS sample:

	document.id('primary').masonry({
	    columnWidth: 100, 
	    itemSelector: '.box' 
	});


Docs
----------

Options:

	document.id('wrapper').masonry({

    	singleMode: false,
    	// Disables measuring the width of each floated element.
    	// Set to true if floated elements have the same width.
    	// default: false

    	columnWidth: 240,
    	// Width in pixels of 1 column of your grid.
    	// default: outer width of the first floated element.

    	itemSelector: '.box:visible',
    	// Additional selector to specify which elements inside
    	// the wrapping element will be rearranged.
    	// Required for Infinite Scroll with window resizing.

    	resizeable: true,
    	// Binds a mooMasonry call to window resizes.
    	// default: true

    	appendedContent: '.new_content',
    	// Additional container element for appended content.
    	// Useful for Infinite Scroll integration.

	});

Events:

	masoned(container): 
		Fires when masonry of the container is complete. contrainer is the wrapper who just got masoned.

Methods:

	Element.masonry(options): 
		Masons the element (which should be a wrapper) with the given options
