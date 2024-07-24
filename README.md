JavaScript (JS) is a high-level, dynamic programming language that is commonly used to create interactive effects within web browsers. It is a core technology of the World Wide Web, alongside HTML and CSS, enabling developers to build web pages that respond to user actions. Key characteristics of JavaScript include:

Interpreted Language: JavaScript code is executed line-by-line by the browser's JavaScript engine.
Event-Driven: JavaScript can respond to user actions such as clicks, form submissions, and mouse movements.
Versatile: It can be used for both client-side (in the browser) and server-side (with Node.js) scripting.
Object-Oriented: Supports object-oriented programming principles.
Prototypal Inheritance: Unlike classical inheritance, JavaScript uses prototypes to share properties and methods between objects.
JavaScript is widely used for web development to enhance user experience, validate forms, create animations, handle asynchronous operations (such as fetching data from a server), and build single-page applications (SPAs) with frameworks and libraries like React, Angular, and Vue.js.


# JavaScript Variables

JavaScript provides three ways to declare variables:

## var

- **Scope**: Function scope
- **Mutability**: Can be redeclared and reassigned

```javascript

var x = 5;
var x = 10; // Redeclaration is allowed
x = 6; // Reassignment is allowed


let
Scope: Block scope
Mutability: Can be reassigned but not redeclared in the same scope

let x = 4;
let x = 6; // Error: Declaration is not allowed in the same scope
x = 5; // Reassignment is allowed

const
Scope: Block scope
Mutability: Cannot be reassigned or redeclared

const x = 7;
x = 9; // Error: Reassignment is not allowed


# JavaScript Data Types

JavaScript has several data types:

## 1) Primitive Types (Immutable)
- **Number**
- **String**
- **Boolean**
- **Null**
- **Undefined**

## 2) Objects
Objects are key-value pairs.
```javascript
let person = {
  name: "person",
  age: 30
};

Arrays
let colors = ["red", "green", "blue"];


3) Variable Assignment
4) Variable Scope
Global Scope: Variables declared outside a function or block have global scope and can be accessed anywhere.
Function Scope: Variables declared within a function can only be accessed within that function.
Block Scope: Variables declared with let and const inside a block can be accessed only within that block.

## JavaScript Operators and Functions

### Arithmetic Operators
They perform basic arithmetic operations.

### Comparison Operators
They are used to compare two values and return a boolean value.

### Logical Operators
They perform logical operations and return a boolean value.
1. Logical AND (`&&`)
2. Logical OR (`||`)
3. Logical NOT (`!`)

### Assignment Operators
They are used to assign values to variables.

### Concatenation Operator
They are used to concatenate two or more strings.

### Conditional (Ternary) Operator
It is used as a shortcut for the `if-else` statement.

### Defining Functions in JavaScript
In JavaScript, you can define a function using the `function` keyword. Functions can be named or anonymous.

#### Named Function
```javascript
function greet(name) {
    console.log(`Hello, ${name}!`);
}


Anonymous Function Expression
let sayHello = function() {
    console.log("Hello");
};


Function Parameters
Function parameters are placeholders for values that you can pass into a function when you call it. They make a function more flexible by allowing it to work with different inputs.


Arrow Function
An arrow function is a concise way to write a JavaScript function in a shorter form. They make our code more structured and readable. Arrow functions are anonymous functions, meaning they do not have a name. They do not return any value and can be declared without the function keyword. They are also called lambda functions.


const demo = () => {
    console.log("Hi");
}


Object and Class
Objects and classes are fundamental concepts that allow you to model and organize your code in a structural and reusable manner.

Objects
In JavaScript, an object is a collection of key-value pairs, where each key is a string and each value can be of any type. They are used to represent entities, data structures, or concepts in our code.

Defining Objects:
1)Using Object Literals: The simplest way to create objects.
let person = { name: "Alice", age: 30 };

2)Using Constructor Functions: These are used to create multiple instances of objects with similar properties and methods.
function Person(name, age) {
    this.name = name;
    this.age = age;
}

let alice = new Person("Alice", 30);
let bob = new Person("Bob", 35);

Classes
Classes provide a more structured and object-oriented way to create objects. They are blueprints for creating objects with predefined properties and methods.
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }

    sayHello() {
        console.log(`Hello, my name is ${this.name}`);
    }
}

Creating Instances:
We use the `new` keyword to create an instance of a class.
```javascript
let alice = new Person("Alice", 40);


# Class Methods and Inheritance in JavaScript

## Class Methods
Methods defined within a class are automatically added to the prototype of objects created from that class. These are called instances of the class.

```javascript
class Person {
  sayHello() {
    console.log("Hello!");
  }
}

const alice = new Person();
alice.sayHello(); // Outputs: Hello!


Inheritance
Classes in JavaScript support inheritance using the extends keyword.

class Animal {
  makeSound() {
    console.log("Some sound");
  }
}

class Dog extends Animal {
  makeSound() {
    console.log("Bark!");
  }
}

const myDog

# JavaScript Arrays and Methods

JavaScript provides a variety of built-in array methods.

## What is an Array?

An array is an ordered list that stores multiple values of different data types. In JavaScript, you create arrays using `[]`.

```javascript
let fruits = ["apple", "banana", "1"];

Arrays are zero-indexed, meaning the first element is at index 0.

Accessing Array Elements
You can access array elements by their index.

Array Methods
push()
Adds elements to the end of an array.

pop()
Removes and returns the last element from an array.

shift()
Removes and returns the first element from an array.

unshift()
Adds elements to the beginning of an array.

concat()
Combines two or more arrays.

join()
Joins all elements of an array into a string.

slice()
Extracts a portion of an array.

splice()
Adds or removes elements from an array at a specific index.

forEach()
Iterates over each element in an array.

map()
Creates a new array by applying a function to each element in the original array.

// Using map() method
const myArray = [1, 2, 3, 4];
const myArrayTimesTwo = myArray.map(function(num) {
  return num * 2;
});

console.log(myArrayTimesTwo); // Output: [2, 4, 6, 8]

Using Arrow Functions with map()

const myArray = [1, 2, 3, 4];
const myArrayTimesTwo = myArray.map((num) => num * 2);

console.log(myArrayTimesTwo); // Output: [2, 4, 6, 8]


# Array Destructuring in JavaScript

Array destructuring allows you to extract values from arrays, properties, and objects and assign them to variables in a more concise and readable way.

## Examples

### Example 1
```javascript
let num = [1, 2, 3];
let [a, b, c] = num;
console.log(a); // 1
console.log(b); // 2
console.log(c); // 3

Example 2
let num = [1, 2, 3];
let [a, , c] = num;
console.log(a); // 1
console.log(c); // 3

Example 3
let num = [1, 2];
let [a, b, c = 0] = num;
console.log(a); // 1
console.log(c); // 0

## Object Destructuring

Object destructuring allows you to extract values from an object and assign them to variables with the same names as the object's properties.

### Example

```javascript
let person = { firstName: "Uj", lastName: "Wala" };

// Destructuring assignment
let { firstName, lastName } = person;

console.log(firstName); // Output: Uj
console.log(lastName);  // Output: Wala


 Accessing Elements
1) getElementById(): Selects an element by its unique ID attribute.
let element = document.getElementById('myId');

2) getElementsByClassName(): Selects elements by their class name.
let elements = document.getElementsByClassName('myClass');

3)getElementsByTagName(): Selects elements by their HTML tag name.
let elements = document.getElementsByTagName('tagName');

4)querySelector(): Selects the first element that matches a CSS selector.
let element = document.querySelector('.className'); // Can be any valid CSS selector

Modifying Element Content
1) textContent and innerHTML: Change the text or HTML content of an element.
element.textContent = 'New text content';
element.innerHTML = '<p>New HTML content</p>';

2)setAttribute(): Set or modify attributes of an element.
element.setAttribute('attributeName', 'attributeValue');
Ex:
<img id="myImage" src="placeholder.jpg" alt="Placeholder Image">
// Select the image element by its ID
let imageElement = document.getElementById('myImage');

// Change the src attribute to a new image URL
imageElement.setAttribute('src', 'newImage.jpg');

// Change the alt attribute to a new description
imageElement.setAttribute('alt', 'New Image Description');

3)style: Modify CSS styles directly.
element.style.color = 'blue';
element.style.backgroundColor = 'yellow';

# DOM Manipulation in JavaScript

## 1. Accessing Elements

- **getElementById()**: Selects an element by its unique ID attribute.
- **getElementsByClassName()**: Selects elements by their class name.
- **getElementsByTagName()**: Selects elements by their HTML tag name.
- **querySelector()**: Selects the first element that matches a CSS selector.

## 2. Modifying Element Content

- **textContent** and **innerHTML**: Change the text or HTML content of an element.
- **setAttribute()**: Set or modify attributes of an element.
- **style**: Modify CSS styles directly.

## 3. Creating and Appending Elements

- **createElement()**: Create a new HTML element.
- **appendChild()**: Add a new child element to an existing element.

## 4. Removing Elements

- **removeChild()**: Remove a child element from its parent.

## 5. Event Handling

- **addEventListener()**: Attach an event listener to an element.

## 6. Traversing the DOM

- **parentNode** and **children**: Access parent and child elements.
- **querySelectorAll()**: Select multiple elements that match a CSS selector.


