##### JavaScript today:
- Web/mobile apps
- real time networking apps
- command line tools
- games
It runs on *browsers* that have JS engines
- firefox: spidermonkey
- chrome: v8
###### *Node*:
- C++ Program that has JavaScript imbedded into it
- includes chrome:v8 engine and run JavaScript code outside of a browser/pass JS code to node for execution/build the backend.
ECMAScript
- is a specification while JavaScript is a programming language that conforms to the specification.
- #ECMA is responsible for defining standards.

Its good to have Node.js on your machine to install third party libraries

Statement in code expresses an action to be carried out
- example [[JS Flow Chart.canvas|JS Flow Chart]]
- // represent comments that you can add descriptions to the code and is ignored by JavaScript engine.
- #Scripts get terminated with a ==***;***==
```
<script>
	// First JavaScript Code!
	- console.log('hello world');
 </script>
```

JavaScript is all about behavior: how should your webpage behave when we hover over our mouse over an element etc.

##### Variables:
- store data in a computer temporarily
- to declare a variable "var" used to be used but now it is =="let"==
- more common to use single quote when declaring strings in JavaScript
```
- let name - 'michele';
- console.log(name);
``` 
- *"let" declares the variable "name" to Michele in the string*
##### - Rules for naming variables:
- cannot be a reserved keyword
	- for example: let, if, var, typeof, return
	- let if=name (would not work)
	- should be meaningful not (a,b1,x)
	- cant start with a number (~~1name~~)
	- cant have a space or hyphen (-)
		- for example: let firstName;
	- Are case sensitive
		- ex: *let FirstName;* is different from *let firstName;*
	 - to delcare multiple variable, on one line by separating using a comma
		- ex: let firtName, lastName;
		- the modern best practice is to declare them on separate lines though
			- let firstName = 'michele'
			- let lastName = 'ferrer'
- Camel Notation: This is the most common naming convention in JavaScript. Variable names start with a lowercase letter, and each subsequent word starts with a capital letter.
- **PascalCase:** Similar to CamelCase, but the first letter of each word is capitalized. This is often used for naming constructors or classes. ex: function.Person(firstName,lastName){}
- **UPPER_CASE:** Used for naming constants. All letters are capitalized, and words are separated by underscores.
- **underscore:* Some developers use underscores to separate words in variable names, especially for private or internal variables.
- **Single letter:** Single-letter variable names are often used in loops or mathematical operations.

##### Variables vs Constants:
- the value of a variable can change, but the value of a constant remains the same.
- defaults values for variables are undefined.
- we are not able to reassign a constant and it will be an error if you try to change `let-> to const`
	- best practice= `const` should be your first choice, otherwise if you need to reassign a variable use `'let'`

##### Primitive Types:
- string-hold text values
- numbers-numeric values
- Array-collection of values
- boolean-true or false
- Object-hold key-value pairs 
- function-hold executable code
- undefined-declared but not assigned a value
- null-var set to null value
`let age = 30; // number literal`
`let isApproved = true; //boolean literal can be true or false`
`let firstName = undefined;`
`let lastName = null; //used to clear the value of a variable`
`let selectedColor = null; // when the user selectes the color then youd change it to 'color'```
`
##### Reference Types:
###### - objects-
- just like in real life
	- Allows you to clean up code to make it cleaner and reference multiple variables with a {} #objects
	- To change a property of the object one way that is used is DOT Notation
	- Bracket Notation- uses square brackets and passes a string that declares target properties
	- Dot notation is more concise and shorter and is default choice. but during the times when you don't know the specifics of target property then bracket notation would be better.
```
//object//
let person = {
// add key properties
name: 'michele',
age: 30
};
//DOT Notation to change specific property
person.name = 'john';
// you can also change console.log(person.name);
console.log(person.name); //changes just the name
console.log(person); //will show the object in console.log
//Bracket Notation 
person['name]='mary';
let selection = 'name';
let mary = 'mary'; // we had to define the name through the variable
person[selection] = mary; //would show up as mary because the variable mary was declared as 'mary'
```

###### - Arrays- you use arrays to store lists of objects:
- 
	- each element has an index which determines the position of that element in the #Arrays 
	- you can expand the length of the array and list of objects in the code as well because it is dynamic. 
	- in JavaScript you can store different types of types of data.
	- #Arrays  are #objects 
	- `console.log(selectedColors.length);` // will show on console the amount of properties that have been declared in the array. 
```
let selectedColors = ['red', 'blue']; //array literal-indicates empty array
//console.log(selectedColors); will show all elements in the array.
/* to access the index of an array you would put square
bracket in the console.log variable and put the index in the bracket */
selectedColors[2] = 'green';
selectedColors[3] = 1;// arrays are not limited to only one kind of element/data types
console.log(selectedColors [0]); //only shows first array which is 'red'
```
###### - Function:
- Fundamental building block in JavaScript
	- a set of statements that performs a tasks or calculates a value.
	- When declaring a function we do not have to use semi colons like for statements or variables (let number=1;)
	- Functions can have inputs and these inputs can change the behavior of the #functions
		- Parameter is what we have at the time of declaration
		- Argument is the actual value that supplies the parameter.
		- Expressions are a call to a function i.e: square
		- '**Return**' statement is used to end the execution of a function and specify the value to be returned by that function.
		- `function add(a, b) {`
			`return a + b;` `}`
			`let result = add(3, 5);`
			`console.log(result); // Output: 8`

```
// performing a task
function greet(name, lastName) { 

/*body of the function where we add statements to define the logic of our application. The "name" is a parameter/input thats only accecible in side of the function. */

console.log('hello ' + name + ' ' + lastName);
}
greet('john', 'smith'); 
/*john is an argument to the great function and name is a parameter to the great function.*/
greet('mary', 'contreras');

// Functions that calculate a value:

function square(number){
    return number * number;
}
// let number = square(2); dont have to declare like this

console.log(square(2)); // there are two function calls here.expressions are a call to a function.
```


---

### Object-Oriented Programming in JavaScript:
- is a way of organizing and structuring code using objects. #OOP is a collection of data (properties) and functions (methods) that can be used to represent real-world entities or concepts. *==(comes up in a lot of interviews and makes you stand out when its in your resume)==*
- -The four pillars are:
	- Encapsulation
		- Encapsulation is the idea of bundling data (properties) and functions (methods) that operate on the data together in a single unit (an object). This helps in organizing and managing code by making it more simpler and increasing its reusability.
	- Abstraction
		- the concept of hiding the complex implementation details of a system and only showing the essential features of an object. It allows you to focus on what an object does, rather than how it does it. Reduces the impact of change with a simpler interface.
	- Inheritance
		- Inheritance is a way to create new classes (subclasses) based on existing classes (superclasses). Subclasses inherit properties and methods from their superclasses, which helps in reusing code and creating a hierarchy of classes. It helps reduce redundant code. 
	- Polymorphism
		- Polymorphism allows objects of different classes to be treated as objects of a common superclass. This means that you can use a single interface (method) to operate on objects of different types.
Before #OOP , there was procedural programming that divided a program into a set of functions, with data stored in a bunch of variables and functions that operate on the data.
Procedural Programming ex:

| f() | x   |
| --- | --- |
| f() | x   |
OOP Encapsulation ex:
```
// Constructor function for creating a Person object
function Person(name, age) {
    // Private variables
    let _name = name;    let _age = age;
    // Public methods to access and modify private variables
    this.getName = function()     {   return _name;     };
    this.getAge = function()      {   return _age;      };
    this.setName = function(name) {  _name = name;      };
    this.setAge = function(age)   {   _age = age;       };
}
// Creating a new Person object
let person1 = new Person('Alice', 30);
// Accessing and modifying private variables using public methods
console.log(person1.getName()); // Output: Alice
console.log(person1.getAge());  // Output: 30
person1.setName('Bob');
person1.setAge(25);
console.log(person1.getName()); // Output: Bob
console.log(person1.getAge());  // Output: 25
```
##### Benefits of OOP:
1. Using encapsulation we group related variables and functions together to reduce complexity and increase reusability. 
2. Abstraction we had the details and complexity and show only the essentials to isolate the impact of changes in the code.
3. inheritance we eliminate redundant code.
4. Polymorphism we refactor ugly switch/case statements

OOP in use:

```
const circle = {
    radius:1,
    location: {
        x:1,
        y:1
    },
    draw: function() {
        console.log("draw");
    }
};
*/ three objects in the const circle: radius, location and draw.
if a member is a function then its referred to as a method ie: draw is a method
*/ radius and location are properties.
```

- object literal syntax is NOT a good method to duplicate if it has more than one method. Because you will have to fix any bugs in all the duplications.
	- if an object has one or more methods the object has **behavior**.
	- the solution to that problem is to use factory or construction syntax
	- Factory Function
		- we use the return operator and camal notation
			`function createCircle(radius){`
			    `return {`
			        `radius, // when the key and value are the same we can remove the code and just leave the key`
			        `draw: function() {`
			        `console.log('draw');`
			        `}`
			        `}`
				 `};`
			    `const circle = createCircle(1);`
			    `circle.draw();`
	- Construction function:
		- utilizes the parse notation where the first letter of the variable is uppercase.
		- in the body of the function instead of using the 'return' statement we use '*this.*'
		- We use the 'new' operator to make return functions happen automatically.
```
	- function Circle(radius){ // circle function is actually an object 
			- this.radius = radius;
			- this.draw = function(){
				- console.log('draw');
			- }
			- }
		- const another = new Circle(1);
```
Functions and objects:
