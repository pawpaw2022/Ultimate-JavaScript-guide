# Ultimate JavaScript Guide

<img style="width:400px" src="https://c.tenor.com/NOYF3f82b_gAAAAC/programmer.gif" alt="Happy Programming, Happy life">

---

## Table of Content

- [Basics](#basics)
  - [Hello World](#hello-world)
  - [Variables](#variables)
  - [Constants](#constants)
  - [Primitive Types-Title](#primitive-types-title)
  - [Dynamic Typing](#dynamic-typing)
  - [Objects](#1objects)
  - [Arrays](#1arrays)
  - [Functions](#1functions)
- [Operators](#operators)
  - [Arithmetic Operators](#arithmetic-op)
  - [Assignment Operators](#assignment-op)
  - [Comparison Operators](#comparison-op)
  - [Equality Operators](#equality-op)
  - [Ternary Operator](#ternary-op)
  - [Logical Operators](#logical-op)
  - [Logical Operators with non-booleans](#logical-op-with-non-booleans)
  - [Bitwise Operators](#bitwise-op)
  - [Operators Precedence](#op-precedence)
- [Control Flow](#control-flow)
  - [If...else](#if-else)
  - [Switch...case](#switch-case)
  - [For](#for)
  - [While](#while)
  - [Do...while](#do-while)
  - [For...in](#for-in)
  - [For...of](#for...of)
  - [Break and Continue](#break-and-continue)
- [Objects](#objects)
  - [Factory Functions](#factory-functions)
  - [Constructor Functions](#constructor-functions)
  - [Dynamic Nature of Objects](#dynamic-nature-of-objects)
  - [Constructor Property](#constructor-property)
  - [Functions are Objects](#functions-are-objects)
  - [Values vs Reference Types](#values-vs-reference-types)
  - [Enumerating Properties of an Object](#enumerating-properties-of-an-object)
  - [Cloning an Object](#cloning-an-object)
  - [Garbage Collection](#garbage-collection)
  - [Math](#math)
  - [String](#string)
  - [Template Literals](#template-literals-es6-new-feature)
  - [Date](#date)
- [Arrays](#arrays)
  - [Adding Elements](#adding-elements)
  - [Finding Elements(Primitives)](#finding-elements-primitives)
  - [Finding Elements(Reference Types)](#finding-elements-reference-types)
  - [Arrow Functions](#arrow-functions)
  - [Removing Elements](#removing-elements)
  - [Emptying an Array](#emptying-an-array)
  - [Combining and Slicing Arrays](#combining-and-slicing-arrays)
  - [The spread operator](#the-spread-operator)
  - [Iterating an Array](#iterating-an-array)
  - [Joining Arrays](#joining-arrays)
  - [Sorting Arrays](#sorting-arrays)
  - [Testing the Elements of an Array](#testing-the-elements-of-an-array)
  - [Filtering an Array](#filtering-an-array)
  - [Mapping an Array](#mapping-an-array)
  - [Reducing an Array](#reducing-an-array)
- [Functions](#functions)
  - [Function Declarations vs Expressions](#function-declarations-vs-expressions)
  - [Hoisting](#hoisting)
  - [Arguments](#arguments)
  - [The Rest Operator](#the-rest-operator)
  - [Default Parameters](#default-parameters)
  - [Getters and Setters](#getters-and-setters)
  - [Try and Catch](#try-and-catch)
  - [Local vs Global Scope](#local-vs-global-scope)
  - [Let vs Var](#let-vs-var)
  - [The this Keyword](#the-this-keyword)
  - [Changing this](#changing-this)

---

## Basics

---

### Hello World

To print out `Hello World` msg on the console using JS.

You can either use Chrome Dev tool or [Node.js](https://nodejs.org/en/)

```js
console.log("Hello world");
```

In your terminal window, type:

```bash
node FILE_NAME.js
```

to run your code.

---

### Variables

- Cannot be a reserved keyword (e.g. `if` `let`)
- Should be meaningful
- Cannot start with a number (1name)
- Cannot contain a space or hyphen (-)

```js
let name = "Paul";
console.log(name);
```

---

### Constants

A constant value cannot be changed

```js
const interestRate = 0.5;
console.log(interestRate);
```

---

### Primitive Types - Title

Primitives/Value Types

- String
- Number
- Boolean
- undefined
- null

```js
let name = "Paul";
let age = 21;
let isApproved = false;
let firstName = undefined; // by default, any type is set to undefined
let selectedColor = null;
```

---

### Dynamic Typing

Any type can be changed in JS

```js
let name = "Paul";
console.log(typeof name);
name = 12;
console.log(typeof name);
```

Output:
**string**
**number**

---

<h3 id="1objects">Objects</h3>

Reference Types

- Object
- Array
- Function

**Object:**

```js
let person = {
  name: "paul",
  age: 21,
};

console.log(person);
console.log(person.name);
console.log(person.age);

// Dot Notation
person.name = "Ben";

// Bracket Notation
person["name"] = "Mary";
```

---

<h3 id="1arrays">Arrays</h3>

```js
let selectedColors = ["red", "blue"];
console.log(selectedColors[0]);
```

---

<h3 id="1functions">Functions</h3>

```js
let name = "Paul";

function greet(name) {
  console.log("hello, " + name);
}

greet(name);
```

---

## Operators

---

### Arithmetic Op

`+`:plus
`-`: minus
`*`: times
`/`: divide
`%`: mod (reminder)
`**`: exponent

`x++`, `x--`: get the x first, then increment/decrement
`++x`, `--x`: increment.decrement first, then get x

---

### Assignment Op

`x++`: x = x + 1
`x+=5`: x = x + 5

---

### Comparison Op

`<`, `>`: greater, less than
`<=`, `=>`: greater, less or equal

---

### Equality Op

`===`, `!==`: strict equality (type + value) _RECOMMANDED!_
`==`, `!=`: loose equality (value)

---

### Ternary Op

```js
let points = 110;
// type = 'gold' if points > 100, else 'silver'
let type = points > 100 ? "gold" : "silver";
```

---

### Logical Op

`&&`: and
`||`: or
`!` : not

---

### Logical Op with non-booleans

Falsy (false) _[JS will treat them as `false`]_:
`undefined`
`null`
`0`
`false`
`''`
`NaN`

Otherwise, it is `true`

Ex:

```js
false || 1;
```

Output:
1

---

### Bitwise Op

`|`: Bitwise OR
`&`: Bitwise AND

```js
const number1 = 4; // 1000
const number2 = 2; // 0010

let number3 = number1 | number2; // 1010
let number4 = number1 & number2; // 0000
```

---

### Op Precedence

```js
let x = 1 + 2 * 3; // x = 7

let y = (1 + 2) * 3; // y = 9
```

---

## Control Flow

---

### If else

```js
if (1 + 1 === 2) {
  //do something
} else if (1 + 1 === 3) {
  // do something else
} else {
  // do something else
}
```

---

### Switch case

```js
let role;

switch (role) {
  case "guest":
    // do something
    break;

  case "master":
    // do something
    break;

  default:
  // no need to break...
}
```

---

### For

```js
for (let i = 1; i <= 5; i++) {
  console.log("hello, world");
}
```

---

### While

```js
let i = 0;
while (i <= 5) {
  //do something
  i++;
}
```

---

### Do While

```js
let i = 0;
do {
  // guaranteed to execute at least 1 time
  i++;
} while (i <= 5);
```

---

### For in

```js
const person = {
  name: "paul",
  age: 21,
};

for (let key in person) {
  console.log(key, person[key]);
}
```

---

### For of

```js
const colors = ["red", "green", "blue"];

for (let color of colors) {
  console.log(color);
}
```

Note: use `For in` loop for Property of the Object
whereas `For of` for element in an array

---

### Break and Continue

`break;`: break out the loop
`continue;`: jump to the next iteration

---

## Objects

**Objects** are collections of key-value pairs

Note: If you are familiar with other programming languages, JavaScript objects are a bit different. You do not need to create classes in order to create objects.

The syntax to declare an object is:

```js
const object_name = {
  key1: value1,
  key2: value2,
};
```

For example, an object can be:

```js
const circle = {
  // int
  radius: 1,
  // another object
  location: {
    x: 1,
    y: 1,
  },
  // boolean
  isVisible: true,

  // function
  draw: function () {
    console.log("draw");
  },
};
```

---

### Factory Functions

```js
//Factory Function
function createCircle(radius) {
  return {
    radius,
    draw() {
      console.log("draw");
    },
  };
}

// create factory function
const myCircle = createCircle(1);

myCircle.draw(); // access method
myCircle.radius; // access property
```

---

### Construtor Functions

```js
// Constructor Function (like a class in Java)
function Circle(radius) {
  this.radius = radius;
  this.draw = function () {
    console.log("draw");
  };
}

// create constructor function
const circle = new Circle(1);

myCircle.draw(); // access method
myCircle.radius; // access property
```

---

### Dynamic Nature of Objects

```js
const circle = {
  radius: 1,
};

// add some new properties
circle.color = "yellow";
circle.draw = function () {};

// delete some properties
delete circle.color;
delete circle.draw;

console.log(circle);
```

---

### Constructor Property

Every `Object` in JS has a `constructor` property, that is used to create this `Object`

Ex:

```js
let x = "";

// under the hood, x is using String() constructor
x = new String();
```

---

### Functions are Objects

Every `function` in JS is an `Object`

```js
function Circle(radius) {
  this.radius = radius;
  this.draw = function () {
    console.log("draw");
  };
}

Circle.call({}, 1);

const another = new Circle(1);
```

---

### Values vs Reference Types

**Primitives** are copied by their _value_

**Objects** are copied by their _reference_

Pass by values:

```js
let num = 10;

function increase(number) {
  number++;
}

increase(num);
console.log(num); // num = 10
```

Pass by reference:

```js
let number = { value: 10 };
function increase2(number) {
  number.value++;
}

increase2(number);
console.log(number); // number = {value: 11}
```

---

### Enumerating Properties of an Object

- use `for (let key in circle)`
- use `for (let key of Object.keys(circle))` (since `for..of` are used in array)
- use `for (let entry of Object.entries(circle))` (collect all key-value pair in an array)

```js
const circle = {
  radius: 1,
  draw() {
    console.log("draw");
  },
};

for (let key in circle) {
  console.log(key, circle[key]);
}

// output: radius 1; draw [Function: draw]

for (let key of Object.keys(circle)) {
  console.log(key);
}

// output: radius draw

for (let entry of Object.entries(circle)) {
  console.log(entry);
}

// output: [ 'radius', 1 ]; [ 'draw', [Function: draw] ]

if ("color" in circle) console.log("yes");
```

---

### Cloning an Object

To copy an Object:

```js
// classic way
const another = {};
for (let key in circle) another[key] = circle[key];

// Object assign method. (add additional properties in {})
const another = Object.assign({}, circle);

// spread operator method.
const another = { ...circle };

console.log(another);
```

---

### Garbage Collection

In JS, we don't need explicitly `deallocate` memory when we finish using an array. (Not like in `C`, but like in `Python`)

This is called JS **Garbage Collection**

---

### Math

[JS Math](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math)

Some important methods:

```js
Math.random(); // random number between 0-1

// Getting a random number between two values
function getRandomArbitrary(min, max) {
  return Math.random() * (max - min) + min;
}

Math.round(1.9); // 2

Math.max(1, 2, 3, 4, 5); // 5
```

---

### String

[JS String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)

`String` is Primitive Type yet it can be wrapped to `Object`

```js
// String primitive type (type: string)
const message = "hi";

// String of Object (type: object)
const message2 = new String("hi");
```

`String` has methods:

Some important methods:

```js
const message = "hello, world";

// locate single char
message[0];

message.includes("h");

message.startsWith("hello");

message.endsWith("orld");

message.indexOf(",");

message.replace("hello", "hi");

message.toLowerCase();

// get rid of all spaces before/after message
message.trim();

message.trimLeft();

message.split(" ");
```

---

### Template Literals (ES6 New Feature)

Template Literals allow us to write paragraphs without using `\n` to seperate lines, much cleaner and easier.

`${...}` allow us to add code/variable, like _f-string_ in Python

```js
let name = "Paul";

const string = `Hi ${name} ${2 + 3}, 

Thanks for joining my mailing list.

Regards,
Ben`;

console.log(string);
```

---

### Date

```js
const now = new Date(); // get current time
const date1 = new Date("May 11 2020 09:00");
const date2 = new Date(2020, 4, 11, 9); // YYYY, MM-1, DD, Hr, Min

now.toDateString(); //'Thu Jan 06 2022'

now.toTimeString(); // '13:19:52 GMT-0800 (Pacific Standard Time)'

now.toISOString(); // '2022-01-06T21:19:52.613Z'
```

---

## Arrays

---

### Adding Elements

```js
const number = [3, 4];

// End
number.push(5, 6); // number = [3,4,5,6]

// Beginning
number.unshift(1, 2); // number = [1,2,3,4,5,6]

// Middle
// starting index, delete count, numbers to insert
number.splice(2, 0, "a", "b"); // number = [1,2,'a','b',3,4,5,6]
```

---

### Finding Elements(Primitives)

```js
const number = [1, 2, 3, 1, 4];

console.log(number.indexOf(1)); // return 0

console.log(number.lastIndexOf(1)); // return 3

console.log(number.includes(1)); // true
```

---

### Finding Elements(Reference Types)

The `find()` method returns the value of the first element in the provided array that satisfies the provided testing function. If no values satisfy the testing function, `undefined` is returned.
[Array.find()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find)

```js
const courses = [
  { id: 1, name: "a" },
  { id: 2, name: "b" },
];

// return false bc reference isn't the same
console.log(courses.includes({ id: 1, name: "a" }));

// find() returns the value of the first element in the array
// that satifies the testing function
const course = courses.find(function (element) {
  return element.name === "a";
});

console.log(course);
```

---

### Arrow Functions

In ES6, we can use Arrow Function to simplify code

```js
const courses = [
  { id: 1, name: "a" },
  { id: 2, name: "b" },
];

// Not using Arrow function:
const course = courses.find(function (element) {
  return element.name === "a";
});

// Using Arrow Function:
const course = courses.find((element) => element.name === "a");
```

---

### Removing Elements

```js
const numbers = [1, 2, 3, 4];

//end
const last = numbers.pop(); // numbers = [1,2,3], last = 4

// beginning
const first = numbers.shift(); // numbers = [2,3], first = 1;

// middle
numbers.splice(2, 2); // starting at index 2, removing 2 elements.
```

---

### Emptying an Array

```js
const numbers = [1, 2, 3, 4];

// Solution 1
numbers = [];

// Solution 2
numbers.length = 0; // array get truncated
```

---

### Combining and Slicing Arrays

```js
const first = [1, 2, 3];
const second = [4, 5, 6];

const combined = first.concat(second); // combined = [1,2,3,4,5,6]

// subarray from index 2 (included) to index 4 (excluded)
const slice = combined.slice(2, 4); // slice = [3,4]

const slice = combined.slice(2); // slice = [3,4,5,6]

const slice = combined.slice(); // slice = combined (copy)
```

==Note: `concat()` and `slice()` copy values if it is _primitive type_, copy reference if it is _reference type_==

---

### The spread operator

`spread operator`, i.e. `...` allows us to quickly copy an array

```js
const first = [1, 2, 3];
const second = [4, 5, 6];

const combined = first.concat(second); // combined = [1,2,3,4,5,6]

// using spread operator
const combined = [...first, "a", ...second, "b"]; // combined = [1,2,3,'a',4,5,6,'b']

const copy = [...combined];
```

---

### Iterating an Array

Iterate an array, we use `for`...`of`, or `forEach`

```js
const numbers = [1, 2, 3, 4];

// for...of, loop the element in the array
for (let number of numbers) {
  console.log(number);
}

// for in, loop the index in the array
for (let index in numbers) {
  console.log(index);
}

// forEach
numbers.forEach((number) => console.log(number));

numbers.forEach((index, number) => console.log(index, number));
```

---

### Joining Arrays

```js
const numbers = [1, 2, 3, 4];

const joined = numbers.join(); // return a string "1,2,3,4"
console.log(joined);

const message = "This is a msg";
const parts = message.split(" ");
console.log(parts);

const combined = parts.join("-");
console.log(combined);
```

---

### Sorting Arrays

Sort Numbers:

```js
const numbers = [3, 2, 1, 4];
numbers.sort(); // [1,2,3,4]

numbers.reverse(); // [4,3,2,1]
```

Sort Objects:

```js
const courses = [
  { id: 1, name: "Node.js" },
  { id: 2, name: "JavaScript" },
];

// sort by name
courses.sort(function (a, b) {
  if (a.name < b.name) return -1;
  if (a.name > b.name) return 1;
  return 0;
});

console.log(courses);
```

---

### Testing the Elements of an Array

```js
const numbers = [1, 2, 3, 4, -1];

// every()
// return true if all element satisfy the critiera
const allPositive = numbers.every((value) => value >= 0);
console.log(allPositive);

// some()
// return true if at least one element satisfy the critiera
const atLeastOnePositive = numbers.some((value) => value >= 0);
console.log(atLeastOnePositive);
```

---

### Filtering an Array

```js
const numbers = [1, 2, 3, 4, -1];

const filtered = numbers.filter((n) => n >= 0); // [1,2,3,4]
```

---

### Mapping an Array

```js
const numbers = [1, -1, 2, 3];

const filtered = numbers.filter((n) => n >= 0); // [1,2,3,4]

// add () outside {}, so js doesn't get confused
const items = filtered.map((n) => ({ value: n }));

console.log(items);
```

Nested `filter()` and `map()`chain:

```js
const numbers = [1, -1, 2, 3];

const filtered = numbers
    .filter((n) => n >= 0)
    .map(n => ({ value: n })))
    .filter(obj => obj.value > 1)
    .map(obj => obj.value);

console.log(items); // [2,3]
```

---

### Reducing an Array

```js
const numbers = [1, -1, 2, 3];

const sum = numbers.reduce((accumulator, currentValue) => {
  return accumulator + currentValue;
});

console.log(sum);
```

---

## Functions

---

### Function Declarations vs Expressions

---

### Hoisting

---

### Arguments

---

### The Rest Operator

---

### Default Parameters

---

### Getters and Setters

---

### Try and Catch

---

### Local vs Global Scope

---

### Let vs Var

---

### The this Keyword

---

### Changing this
