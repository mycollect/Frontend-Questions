Frontend-Developer-Code-Questions
=================================

```sh
var a = ‘name’;
b = a;
a = null;

what does b have?
```
```
var x = NaN;
what is x === NaN?
why is it false?
```
```sh
outerFunction(){
    outerVar;
    innerFunction(){
        innerVar;
    }
}

will outerFunction have access to innerVar and vice versa?
```
```sh
var a = “hello”;
a.abc = “world”;
what will a.abc return?
```

Play with display and float values by having some divs as siblings. See how display:block/inline/inline-block will render the divs. Float:left vs display:inline-block - how do they vary. Try all those with following code.
```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		body{
			margin: 0px;
			padding: 0px;
			border: 0px;
		}
		#div1{
			width: 300px;
			height: 300px;
			background-color: red;
			cursor: pointer;
			/*margin: 100px;
			padding: 100px;*/
			display: inline-block;			
			/*clear: right;*/
		}
		#div2{
			width: 150px;
			height: 150px;
			background-color: green;
			/*position: fixed;
			bottom: 10px;
			right: 10px;*/
			display: inline-block;			
			/*clear: both;*/
		}
		#div3{
			width: 150px;
			height: 150px;
			background-color: blue;
		}
		div{
			
		}
	</style>	
</head>
<body>
	<div id="div1">
		
	</div>
	<div id="div2">
		
	</div>
	<div id="div3">
		
	</div>
</body>
</html>
```

Play with position values by having some divs as parent-child. See how position:relative/absolute/fixed/static will render the divs. what's the default position value when nothing given - How does the events vary when clicked on child elements when positioned outside etc. Try all those with following code.
```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		body{
			margin: 0px;
			padding: 0px;
			border: 0px;
		}
		#outer{
			width: 300px;
			height: 300px;
			background-color: red;
			cursor: pointer;
			/*margin: 100px;
			padding: 100px;*/
		}
		#inner{
			width: 150px;
			height: 150px;
			background-color: green;
			/*position: relative;*/
			bottom: 10px;
			right: 10px;
		}
		div{

		}
	</style>	
</head>
<body>
	<div id="outer">
		<div id="inner">
			
		</div>
	</div>
</body>
<script>
		var x = document.getElementById("outer");
		console.log(x);
		x.onclick = function(){
			alert("clicked");
		}
	</script>
</html>
```


Frontend-Developer-Typical-Questions
=================================
```
What is a Doctype and why do we need it?
```
```
List down ways of improving a website's performance?

Minimize HTTP Requests 
Use CDN - cached by other websites
Gzip contents - size reduces by 70% - apache mod_gzip
expires header - static components infinite year and dynamic appropriate datetime
styles at top as page loads progessively
scripts at bottom - as they will block if huge
No css expressions - calculation in css performance hit
external css and js - can be cached and html file size reduces
minified js and css - size reduces
Reduce DNS lookups. Don't included assets from several domain names as it has to lookup dns for all of them
configure ETags - Entity Tags - ETag is a string that uniquely identifies a specific version of a component.
Flush the Buffer Early - php flush() will send the page that's built till then. useful if you send till head so that css gets loaded.
GET for Ajaxes as GET is single package while POST is 2 step - one headers and other data
tinypng
jpegtran
```
```
Explain CSS box model 
```
```
What is Quirks mode?
```
```
What's new in HTML5?

https://developer.mozilla.org/en/docs/web/Guide/HTML/HTML5

DTD declaration made simple
< !doctype html> 

Introduced new Video and Audio Tags - and made embedding video and audio so easy
    <audio controls="">
      <source src="audiofile.mp3" type="audio/mpeg">
    </audio>
    <video width="450" height="340" controls="">
     <source src="videofile.mp4" type="video/mp4">
    </video>

Canvas element
Canvas is used to draw graphics using scripting languages like javascript; It's a container for graphics, images etc.
It's similar to <div>, <a>,<ul> except that contents are rendered through javascript.
```
```
How to make popup close when clicked outside?
```
```
Types of Storage in HTML5

To check if Storage is supported or not, check typeof(Storage) - this should return function
If Storage is supported, there are 2 types - localStorage and sessionStorage
    window.localStorage - stores data with no expiration date
    code.sessionStorage - stores data for one session (data is lost when the tab is closed)
You can access them by using setItem, getItem and removeItem functions.

The localStorage object stores the data with no expiration date. The data will not be deleted when the browser is closed, and will be available the next day, week, or year.

The sessionStorage object is equal to the localStorage object, except that it stores the data for only one session. The data is deleted when the user closes the browser window.
```
```
What are Block and inline elements? 
Followup: Inline-block vs inline vs block
A div with width 50%, what's the difference between float:left and display:inline-block;
```
```
What's Semantic HTML? Can you name some of semantic tags and their significance?
```
```
Why no cross browser and how is it achieved?
What's cross origin policy? How can we achieve it? 
What are all possible ways of doing this?
Explain CORS? How does it work?
Jsonp vs json how does it allow?
```
```
if you wanna search for an element in a page, will Jquery select tag be preferred or native js?
```
```
What happens when a URL is typed? How will a web page be served? Full cycle?
http://igoro.com/archive/what-really-happens-when-you-navigate-to-a-url/
```
```
How does a browser show a webpage. What are there in browser

The browser's main components are:

The user interface 
    this includes the address bar, back/forward button, bookmarking menu etc. Every part of the browser display except the     main window where you see the requested page.
The browser engine - 
    the interface for querying and manipulating the rendering engine.
The rendering engine - 
    responsible for displaying the requested content. For example if the requested content is HTML, it is responsible for      parsing the HTML and CSS and displaying the parsed content on the screen.
Networking - 
    used for network calls, like HTTP requests. It has platform independent interface and underneath implementations for       each platform.
UI backend - 
    used for drawing basic widgets like combo boxes and windows. It exposes a generic interface that is not platform           specific. Underneath it uses the operating system user interface methods.
JavaScript interpreter. 
    Used to parse and execute the JavaScript code.
Data storage. 
    This is a persistence layer. The browser needs to save all sorts of data on the hard disk, for examples, cookies. The      new HTML specification (HTML5) defines 'web database' which is a complete (although light) database in the browser.
```
```
Event delegation ul and li event bubbling
```
```
Which events will bubble and which events do not?
```
```
Jquery fadein implementation - setInterval and clearInterval
```
```
What is a User agent? What information is stored in it? How do the server know from where's the request is coming in?
```
```
What goes as part of headers?
```
```
Cookies vs local storage
Can server modify cookies?
Serverside cookies
```
```
Css position values n explain: relative, absolute, fixed, static
how will 2 divs having same position value will be seen?
```
```
Css display values and explain
inline, inline-block, block, none
```
```
What's the difference between display:none and visibility: hidden?
```
```
When you are adding dynamic elements to a DOM, browser will redraw every time a new element is added. How can I add 5 elements dynamically with just a single redraw?

What's Document fragmentation
```
```
What are Data- attributes? 
```
```
Browser painting and redraw and how to avoid
```
```
Css selectors specificity
.class #id{} or #id .class{}
```
```
types of selectors?
Pseudoselectors
```
```
Inheritence vs composition
```
```
What are Flags to cookies? How can we set them?
```
```
Write class structure in JavaScript 
```
```
New String(x) === New String(x) false why?
```
```
Body.onload vs document.ready
```
```
Body.onload and document.ready which of them is jquery
```
```
Person class and extend to Employee
```
```
Var x=NaN, x===NaN?
```
```
Bind vs live
```
```
Css transitions
```
```
Css 2D & 3D Transforms

CSS 2D Transforms
-----------------
translate()
rotate()
scale()
skew()
matrix()
more on CSS 2D transforms http://www.w3schools.com/css/css3_2dtransforms.asp

Function	            Description
matrix(n,n,n,n,n,n)	    Defines a 2D transformation, using a matrix of six values
translate(x,y)	        Defines a 2D translation, moving the element along the X- and the Y-axis
translateX(n)	        Defines a 2D translation, moving the element along the X-axis
translateY(n)	        Defines a 2D translation, moving the element along the Y-axis
scale(x,y)	            Defines a 2D scale transformation, changing the elements width and height
scaleX(n)	            Defines a 2D scale transformation, changing the element's width
scaleY(n)	            Defines a 2D scale transformation, changing the element's height
rotate(angle)	        Defines a 2D rotation, the angle is specified in the parameter
skew(x-angle,y-angle)	Defines a 2D skew transformation along the X- and the Y-axis
skewX(angle)	        Defines a 2D skew transformation along the X-axis
skewY(angle)	        Defines a 2D skew transformation along the Y-axis


CSS 3D Transforms
-----------------
rotateX()
div {
    -webkit-transform: rotateX(120deg); /* Chrome, Safari, Opera */
    transform: rotateX(120deg);
}

rotateY()
div {
    -webkit-transform: rotateY(130deg); /* Chrome, Safari, Opera */
    transform: rotateY(130deg);
}
```
```
Css animation vs js animation which is recommended

CSS Animations/Transitions were preferred and spoke about loudly that they support hardware acceleration and mobile friendly experience. However not all animations can be achieved using css transformations. Eg. How can you do a continuous scaling and rotate on hover? This is possible only in JS 

More comprisons on http://css-tricks.com/myth-busting-css-animations-vs-javascript/
```
```
Call vs Apply

While the syntax of this function is almost identical to that of call(), the fundamental difference is that call() accepts an argument list, while apply() accepts a single array of arguments.

The apply() method calls a function with a given this value and arguments provided as an array (or an array-like object).
fun.apply(thisArg, [argsArray])

The call() method calls a function with a given this value and arguments provided individually.
fun.call(thisArg, arg1, arg2, ...)


```
```
Looping thru array of characters - ways of looping , for, for each, map?
```
