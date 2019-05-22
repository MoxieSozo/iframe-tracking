# iframe-tracking
Postmessage system for iframe tracking via GTM.

[View Demo](https://moxiesozo.github.io/iframe-tracking/)

## Requirements
In order to use this system of passing events and information between 2 frames you must have access to add or modify javascript on both the parent page and the iframe. 

This can be accomplished either through GTM containers or direct file access. 

There are no other dependencies or frameowrks used -- pure javascript.

## How to use

### Direct

**Parent Frame**

1. Include the parent-scripts.js file at the bottom of the body tag of the page on which the iframe will be embedded.


**Iframe** 

1. Include the iframe-scripts.js file at the bottom of the body tag within the iframe being loaded into the page
2. Call the function in one of two ways by adding the following code insite a script tag below the iframe-scripts.js file. 
	3. Fire an event when the iframe first loads: `post_message('event_name', 'extra info');`
	4. Fire en event on a standard DOM event (e.g. a click):* `document.getElementById('target_id').addEventListener("click", post_message('event_name', 'extra info') );
`


**Iframe Confirmation** 

If the form loads a new page follow the instructions below. Otherwise you will likely need to attach the confirmation using the event listener method outlined above. 

1. Include the iframe-scripts.js file at the bottom of the body tag within the iframe confirmation page. 
	2. This is typically the URL of the action property on the from.
2. Call the function in one of two ways by adding the following code insite a script tag below the iframe-scripts.js file. 
	3. Fire an event when the confirmation loads within the frame: `post_message('event_name', 'extra info');`
	4. Fire en event on a standard DOM event (e.g. a click): `document.getElementById('target_id').addEventListener("click", post_message('event_name', 'extra info') );
`
 

### GTM
Instructions coming soon.


## Demo

An example using direct implmentation (without GTM) can be viewed [here](https://moxiesozo.github.io/iframe-tracking/).

## Files

* **/demo/index.html** - parent frame
* **/demo/iframe.html** - iframe
* **/demo/iframe-thanks.html** - iframe confirmation


