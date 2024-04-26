
[COP2500_2 (1).pptx](https://1drv.ms/p/s!AhStIg7NdoT0hSre81d1WQp7j_in?e=Q6QoWg&nav=eyJzSWQiOjMwNSwiY0lkIjo0MDc3NDU4OTkyfQ)

# JavaScript Fundamentals
##### -  Java script 
	- #JavaScript 
	 - General purpose scripting language for Web pages
	 - Allows for user interaction to enhance static HTML pages
	 - Developed by Brendan Eich at Netscape in 1995
	 - Client-side language; works in the browser of the local computer, not on a server
	 - Programs are executed by a JavaScript interpreter in the browser     
		- JavaScript cant..:
			- Cannot read or write files on a local machine or server
			- Cannot open or close other browser windows opened by another application
			- Object based but not object-oriented
##### JavaScript<>Java
- Developed by Netscape Developed by Sun Microsystems
- Embedded in a Web page Independent of a web page. [[Picture Examples of Intro JS.canvas|Picture Examples of Intro JS]]
- Must be run in a browser No browser required
- Loosely typed language; flexible Strongly typed language; strict guidelines
- Variables, parameters, and function return types do not have to be declared Data types must be declared
- Interpreted by a JavaScript engine in a browser Programs are compiled

==JavaScript is not JAVA====

JavaScript<>HTML
- Can be embedded in an HTML document
- Has its own syntax and rules
- Expects statements to be written in a specific format
- Does not understand HTML but can contain HTML  

##### JavaScript program Usages:
- Detect and react to user-initiated events (e.g. mouse rolls over a link or graphic)
- Improve Website usability with
    - Navigational aids
    - Scrolling messages
    - Rollovers
    - Dialog boxes
    - Dynamic images
- Control the appearance of a page
- Data validation
- Reads and writes Cookie values

#####  **Conditional Statements and Control Flow:** 
- #Controlflow and conditional statements are used to perform different actions based on different conditions. JavaScript supports `if`, `else`, `else if`, `switch`, `for`, `while`, and `do...while`.statements. 
- The `break` statement is used to exit a loop, while the `continue` statement is used to skip the current iteration and proceed to the next one. For example: 
```javaScript
- let num = 10;
	if (num > 0) {
    console.log("Positive number");
	} else if (num < 0) {
    console.log("Negative number");
	} else {
    console.log("Zero");
	}
```

##### Request Response Loop
- #loop user request a Webpage by typing in an address in the URL text box of a browser
- HTTP request is transmitted
- Web server responds returning the file to the client’s browser
- HTML tags render the Web page
- Embedded JavaScript is handled by JavaScript interpreter
##### Asynchronous JavaScript
- #AJAX was established by Jesse James Garret in 2005
- Has existed since 1996
- Creates fast interactivity without waiting for a response from the server
- Allows for partial rendering of Web pages as the response is executed (e.g. google maps)[[Picture Examples of Intro JS.canvas|Picture Examples]]


##### Variable:
- #Variables are used to store data values. In JavaScript, you can declare a variable using the `let` keyword
```
- let message = "Hello, World!";
```

##### Data Types:
- JavaScript supports several #datatypes, including numbers, strings, booleans, arrays, and objects.
	###### - #Arrays and Objects
	- Arrays are ordered collections of values, while objects are collections of key-value pairs.
	- You can access and manipulate array elements and object properties using square brackets (`[]`) or dot notation (`.`).
```JavaScript
- let num = 10;
	let name = "Alice";
	let isStudent = true;
	let fruits = ["apple", "banana", "orange"];
	let person = { name: "Bob", age: 25 };
```
##### Functions:
- #Functions are blocks of code that perform a specific task. You can define a function using the `function` keyword.
- Arrow functions (`() => {}`) provide a more concise syntax for writing functions, especially for simple one-liners.
```JavaScript
- function greet(name) {
    console.log("Hello, " + name + "!");
	}
	greet("Alice");
```
##### Event Handler
- #Eventhandling through JavaScript allows you to respond to user actions, such as clicks and keystrokes, using event handlers. For example:(e.g. button clicked)
```JavaScript
- document.querySelector("button").addEventListener("click", function() {
    console.log("Button clicked!");
	});
```
- [[Picture Examples of Intro JS.canvas|Picture Examples]]
- JavaScript provides the `try...catch` statement for handling exceptions and errors in your code.
- Proper error handling is essential for debugging and ensuring that your application remains stable and functional.
##### Document Object Model #DOM :
- The browser’s stored interpretation of an HTML page
- Structured like a family tree
- Each element of the tree is related to another element, called node
- You can use JavaScript to add, remove, or modify elements on a web page
```JavaScript
- let paragraph = document.createElement("p");
	paragraph.textContent = "This is a new paragraph.";
	document.body.appendChild(paragraph);
```
##### Validation:  
- It is important to find #validation tools to verify that your markup is correct, especially when conforming to the DOM and W3C standards. There are a number of free tools on the Web to help you make sure your markup is valid.
- Two common tools:
	- W3C Validation Tool
    - http://validator.w3.org/check
	- Validome Validation Tool
    - http://www.validome.org
- Checks the markup validity of Web page documents
##### Three layers to a #Webpage

- Content or structural layer
    - HTML/XML #HTML 
- Style or presentation layer
    - Cascading Style Sheets (CSS) #CSS
- Behavior layer
    - #JavaScript
- Unobtrusive JavaScript
    - JavaScript is in a different file than the HTML code [[Picture Examples of Intro JS.canvas|Picture Examples]]
##### Impacts:
- World Wide Web Consortium (W3C)
    - Group of Web designers and programmers who created a set of standards or specifications for all browser manufacturers to follow
    - URL: www.w3.org
    - HTML4 released near the end of 1990s
- European Computer Manufacturers Association #ECMA 
    - Next path was to reformulated HTML in XML terms 
    - Worked with Netscape to provide an international standardization of JavaScript
    - Guarantee one standard version of JavaScript available to companies producing Web pages
   
#### Basic #HTML structure
- Top element is always `<html></html>`
    - Head element contains general information about the document <head></head>
    - Body element contains all content of the Web page `<body></body>`
    - to start a new file: ==index.html==
	- Example:
```html
<!DOCTYPE html>
	 <html>
	 <head>
    <title>Sample Page</title>
	</head>
		<body>
	    <h1>Hello, World!</h1>
	    <p>This is a sample paragraph.</p>
		    <ul>
	        <li>Item 1</li>
	        <li>Item 2</li>
	        <li>Item 3</li>
		    </ul>
		    <a href="https://www.example.com">Visit Example</a>
	    </body>
	</html>
```
##### JavaScript in HTML
- Insert JavaScript in the head or body
- Inserted internally or use external file
- to extract a new JS file: ==index.js==
- [[JS Flow Chart.canvas|JS Flow Chart]]
- example:
```html
<!DOCTYPE HTML>  
	<html>​
	<head>​
		<script type=“text/javascript” src=“welcome.js”>​
		</script>​
		<script language=“javascript” src=“welcome.js”>​
		</script>​
		<script src=“welcome.js”>​
		</script>​
	</head>​
	<body>​
		<script type=“text/javascript”>​
		document.write(“<h2>This is COP 2500 Concepts in Computer Science”</h2>);​
		</script>​
	</body>​
	</html>​
```
<html>  
<head>  
<script type=“text/javascript” src=“welcome.js”>  
</script>  
<script language=“javascript” src=“welcome.js”>  
</script>  
<script src=“welcome.js”>  
</script>  
</head>  
<body>  
<script type=“text/javascript”>  
document.write(“<h2>This is COP 2500 Concepts in Computer Science”</h2>);  
</script>  
</body>  
</html>
 

 
[COP2500_3.pptx](https://1drv.ms/p/s!AhStIg7NdoT0hS3tzQYMNuLlWwJO?e=3TQH3C&nav=eyJzSWQiOjMxNSwiY0lkIjozODE0OTE4NTU4fQ)