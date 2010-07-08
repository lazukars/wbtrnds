wbtrnds
=======

wbtrnds is a simple jQuery plugin.  It allows devlopers to easily select html elements, add a click event to those elements, and fire the Webtrends' dcsMultiTrack() when those selected elements are clicked.

This was created in order to quickly add numerous dcsMultiTrack() functions to a page.

Usage
-----

The .wbtrnds( settings ) plugin takes one argument, settings; it must be an object.  The first property, within the settings object, ie frog, is the class name of the html element that you would like to select.  The url/name properties, are the arguments that will be passed to the dcsMultiTrack() function.   

	$('img').wbtrnds({
			frog : { url : '/example/frogs/', name : 'Frogs' },
			bees : { url : '/example/bees_commercial/', name : 'Bees' }
	});

	<img class='frog' src="/images/frog.jpg" alt=""/>
	<img class='bees' src="/images/bees.jpg" alt=""/>

Now, for instance, when a user clicks on:

	<img class='frog' src="/images/frog.jpg" alt=""/>

dcsMultiTrack('DCS.dcsuri', '/example/frogs/', 'WT.ti' , 'Frogs'); will fire

Todo
----

Enabling this plugin to work with attributes other than classes.



	






