# dom-manipulation
research about DOM manipulation

1.	Using javascript to create HTML elemnts

To create a custom HTML element:
  ``` script
	document.registerElement()
  ```
  registerElement() could be passed a String defining the name of that Element


This returns HTML elemnt, as an example:

	var buttonElement = document.registerElement('button-element');

To append this element to HTML
	document.body.appendChild(new buttonElement());

So the ouput of :

	var buttonElement = document.registerElement('button-element');
	document.body.appendChild(new buttonElement());

should be
``` HTML
	<body>
		<button-elemnet>
		</button-element>
	</body>
  ```

if for example we named the element 'p'? Would it act like the common paragraph element?

2. Replacing an HTML element using .replaceChild(...) ->
``` HTML
	<script type="text/JavaScript">

	  var myAnchor = document.getElementById("myAnchor");
		// bring something to replace <In this case we are replacing an anchor>
	  var mySpan = document.createElement("span");
		// create something to replace with <In this case we created a span>
	  mySpan.innerHTML = "replaced anchor!";
		// body of span
	  myAnchor.parentNode.replaceChild(mySpan, myAnchor);
		// replace myAnchor in the parent node of myAnchor with mySpan
		// select the parentNode of myAnchor, replace one child of this parent 'myAnchor' with mySpan
	</script>
  ```


		/***OR***\
  ``` HTML
	// DOUBTFUL!!!
	<script type="text/JavaScript">

	  var str = '<element [options]>Contents</element>';
		// created the element in the form of String
	  var Obj = document.getElementById('TargetObject');
		// cought the element we want to replace
	  Obj.outerHTML = str;
		// replace the outerHTML with str which represents a new element
		// while innerHTML returns the contents of the element,
    // outerHTML returns the contents+the tag
	</script>
  ```
3.
``` text
How would you add an <li> to <ul>?
To add an <li> to <ul> is by:
```
``` javascript
		function pushli(contents) {
			var newli = document.registerElement('li');
			document.ul.appendChild(new newli());
		}
```


## Events
- Events are "thing" that happens to HTML page.
- When JS is used in that HTML page, it can "react" on that event.
- Examples of events:
   - HTML page finished loading.
   - HTML input field was changed.
   - HTML button was clicked.
- Events can add changes to the content of an element.

- Sometimes the code can change its own element using this.innerHTML.
- Sometimes event attributes are used to call functions since JS code sometimes is lengthy.

## What can JS do?
- Event handlers can be used to handle user input and user and browser actions.
## What those actions might be?
- Things that should be done everytime a page loads or closed.
- When user clicks a button or inputs data.

## Methods to allow JS work with events?
- HTML event attributes (onload, onunload,  onafterprint, etc...) can execute JS code directly.
- HTML event attributes can call JS functions.

## Event.preventDefault()
- This event interface's method tells the user agent (the browser) if an event isn't explicitly handled then it's default action should not be taken as it normally should be.
- The event continues working until one of it's eventListeners calls stopPropagation() or stop immediatePropagation().
