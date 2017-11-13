# dom-manipulation
research about DOM manipulation

1.	Using javascript to create HTML elemnts

To create a custom HTML element:
  ```
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


		_***OR***_
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
  ```
  ```
3.
``` text
How would you add an <li> to <ul>?
To add an <li> to <ul> is by:
```
	```javascript
		function pushli(contents) {
			var newli = document.registerElement('li');
			document.ul.appendChild(new newli());
		}
```
