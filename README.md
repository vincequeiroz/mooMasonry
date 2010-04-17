mooMasonry
===========

mooMasonry is a layout plugin for Mootools. Think of it as the flip side of CSS floats. Whereas floating arranges elements horizontally then vertically, mooMasonry arranges elements vertically then horizontally according to a grid. The result minimizes vertical gaps between elements of varying height, just like a mason fitting stones in a wall.

![Screenshot](http://github.com/orefalo/mooMasonry/raw/master/Logo.png)

Comparison Example
------------------

CSS Floats
![Screenshot](http://github.com/orefalo/mooMasonry/raw/master/screen1.png)

mooMasonry
![Screenshot](http://github.com/orefalo/mooMasonry/raw/master/screen2.png)

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

Implements:

	Options, Events

Syntax and options:

	var cp = new MooColorPicker(container, options);
	
	container: 
		The <div> container (will be empty).
	
	options (object, optional): 
		Initial options for the class. Options are:
			colors: An array of strings, like ["#0123456", "#789ABC"].
			defaultColor: Index of preselected color 
				(default -1, none).
			className: CSS class for single color <div> boxes 
				(default 'moocolorcheckbox').
			selectedClassName: CSS class for selected color <div> box 
				(default 'moocolorcheckbox_selected').

Events:

	masoned(container): 
		Fires when masonry of the container is complete. contrainer is the wrapper who just got masoned.

Methods:

	Element.masonry(options): 
		Masons the element (which should be a wrapper) with the given options
