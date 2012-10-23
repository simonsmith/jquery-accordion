# jQuery Accordion
A really simple accordion that I wrote for a work project because the jQuery UI version requires 1500+ lines of code, and that's unacceptable for responsive design.

## Usage
Two ways:

__AMD Style__ (better!)

```js
require(['path/to/Accordion'], function(Accordion) {
	new Accordion('.some-container', {
		// options
	})
});
```
Ensure you have set a path to `jquery` in `require.config` (but you knew that already!)

__Standard Style__ (less awesome)

```js
$.accordion('.some-container', {
   // options
});
```
Doesn't really follow the traditional jQuery plugin style, but I prefer AMD so this was just a quick addition for non-AMD users :)

## Methods
Supports `openAllPanes` and `closeAllPanes`

Example
```js
var accord = $.accordion('.selector');

$('button.open').on('click', function(){
    accord.openAllPanes();
});

$('button.close').on('click', function(){
    accord.closeAllPanes();
})​;
```

## Options

```js
{
	 // Currently open pane
    openClass: 'is-active-pane',   
     
    // Attached to the container when accordion is ready
    activeClass: 'accordion-active', 
    
	// Anything that can be passed to jQuery animations  
    animSpeed: 'fast',
    
	// Which pane to open by default
    openPane: 0,
    
	// What elements to use
    selectors: {
        item: '.accordion-item',
        header: '.accordion-header',
        content: '.accordion-content'
    }
}
```

## Demo

Fiddle away! - http://jsfiddle.net/Blink/QwX8J/
