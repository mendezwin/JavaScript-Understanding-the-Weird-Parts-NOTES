# JavaScript: Understanding the Weird Parts - NOTES

These are notes covering the important topics in the JavaScript: Understanding the Weird Parts course. 

Having an understanding of these topics help understand how JavaScript works under the hood, and how JavaScript frameworks such as Angular, jQuery, or React are made. 

A more detailed version of the topics covered, can be found by reading the book "Speaking JavaScript". 

Topics Covered in JavaScript: Understanding the Weird Parts:
- Execution Contexts and Lexical Environments
- Types and Operators
- Objects and Functions
- Object Oriented JavaScript and Prototypal Inheritance
- Building Objects
- Odds and Ends
- Brief JavaScript ES6 review.

## Execution Contexts and Lexical Environments

### Syntax Parser
A program that reads your code and determines what it does and if it's grammar is valid. 

The parser translates it to something the computer can understand. 

### Lexical Environment 
Where something fits physically in the code you write. 

### Execution Context
A wrapper to help manage the code that is running. 

### Name / Value Pair
A name which maps to a unique value. 

Example:
```
var address = '100 Main St';
```

### Object
A collection of name value pairs. 

The Global Object in JS is represented by '**this**'.

In JavaScript when you create variables and functions, those values get attacjed to the global variable.

### The Execution Context
Creation and **Hoisting**. 
If you have any variables defined in the function scope, it will be brought to the very top. Declare your variables on top of the function.

**undefined** in JavaScript means the variable has not been set.

### Single Threaded
One command is executed at a time. 

### Synchronous
One at a time and in order.

### Invocation
Running a Function by using parenthesis.

Every context creates a execution context and they are stocked.

Scope chain is the process of going your execution context.

### Scope
Where a variable is available in your code. 

'let' in ES6 allows for block scoping.

### Asynchronous
More than one at a time. 

**event** queue happens after something happens in JavaScript. Like a click reuqest.

```
document.addEventListener('click', clickHandler)
```

## Types and Operators
### Dynamic Typing
You don't tell the JavaScript engine what type of data a variable holds, it figures it out while your code is running. 

### Static Typing
Define the data type beforehand. (ie. Java)

**undefined** a lack of existence 
**null** a lack of existence
**bool** true or false
**number** floating point number


## Objects and Functions
Use the Dot operator when defining properties in objects.

**Namespace:** A container for variables and functions. 

Use objects to create containers for variables that might be conflicted. 

**JSON:** JavaScript Object Notation

Convert object to JSON String.
```
JSON.stringify
```

Converts to JSON.
```
JSON.parse
```

Functions are objects in JS.

### First Class Functions
Everything you can do with other types, tou can do with functions. 

### Expression
A unit of code that results in a value. 

### Anonymous function 
A function that doesn't have a name. 

### By Value vs By Reference
You can set the value of a variable by refering another. 

### Mutable
To change something.

### Execution Context
When the code is executed.

### Object Literal
A JavaScript Object with properties. 

'**this**' refers to the execution context. 

A function inside a function in a object literal refers to the window object.

Arrays can contain any type of data because it is untyped. 

### Arguements
The paramaters you pass to a function.

You can set default values to parameters in future JS parameters.

Call the arguement by using the "arguements" object in JS. 

'**...spead**' takes a series of arguements and creates a array.

Semicolons are optional in JavaScript. 

JavaScript will enter a semicolon for you on statements when you press enter.

### Immediately Invoked Function Expressions (IIFE)
Running a function expression after defining it. 

```
var greeting = function (name){
    return 'Hello ' + name;
}();

Notice the the () call. 
```

### Closures
An inner function that has access to the outer (enclosing) functions variables. Accessed through the scope chain. 

### Function Closures
Closures are commonly used to give objects data privacy.

### Function Factories
A function used to run another function.

### Callback Function 
A function you give to another function to be run when the other function is finished. 

Using setTimeout is an example of a callback function. 

### .call(), .apply(), .bind()

Function object in JS composes of: 
- "Invocable" - code.
- NAME. optional can be anonymous.
- call() apply() bind()

**.bind** - Combines objects to allow functions and properties to be accessible. It defines the "**this**" in a function.
**.call** - Same as bind, but it executes. 
**.apply** - Same as call, but it expects an array of values.

```
Object1.functionName1.apply(Object2)

```
So we want to use the function in Object1, but with Object2. The 'this' keyword will now work with Object 2 as Object2.functionName1. 

### Function Currying 
Creating a copy of a function, but with some preset parameters.

Use UnderScore/LoDash for additional functionality. 

## Object Oriented JavaScript and Prototypal Inheritance
### Inheritance
One objects gets access to the properties and methods of another object.

### Classical Inheretance
Used in many popular OOP languages like Java. It is Vebose. 
```
verbose, private, protected, friend, etc
```

### Protypal Inheritance
Simple, flexible, extensible, easy to understand. 

All objects have a property function called __proto__.

Prototype instances are accessible with new object instances. 

Everything is an object. 

"for in" loops through all properties in a object.

Create objects using the "new" keyword. 

"new" creates an empty object. 

### Function Constructors
A normal function that is used to constant object. 

In good written JS code you will find properties declared in the object, and functions using prototype functions. 

Use function constructors with a capital, so that you know when you're creating a object. Easier for "new" keyword. 

```
function Box(col)
{
   var color = col;

   this.getColor = function()
   {
       return color;
   };
}
```

```
var blueBox = new Box("blue");
alert(blueBox.getColor()); // will alert blue

var greenBox = new Box("green");
alert(greenBox.getColor()); // will alert green
```

JavaScript comes with standard built-in objects with constructors. 

They also have prototype properties.

Example: String.Date

## Building Objects

### Object creation

Object.create to create an empty object. 

You can set values by passing a object constructor. 

```
function person(){
    // Code goes here
}
Object.create(person)
```

### Polyfill
Code that adds a feature which the engine may lack. 

### Class Object in JavaScript
"class" is an object in JavaScript

### Extends Object in JavaScript
"extends" sets the prototype in JS.

## Odds and Ends
### Syntatic Sugar
A different way to type something that doesn't change how it works under the hood. 

### Type of
"**typeof** variableName" will show you what data type it is. 

### Use Strict
"use strict" to declare strict rules JavaScript code runs. 

## Brief JavaScript ES6 review.




