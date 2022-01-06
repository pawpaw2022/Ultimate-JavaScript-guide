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
  - [Object](#object)
  - [Arrays](#arrays)
  - [Functions](#functions)
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
  - [Basics](#basics)
  - [Basics](#basics)
  - [Basics](#basics)
  - [Basics](#basics)
- [Arrays](#arrays)
  - [Basics](#basics)
- [Functions](#functions)
  - [Basics](#basics)
  - [Basics](#basics)

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

### Object

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

### Arrays

```js
let selectedColors = ["red", "blue"];
console.log(selectedColors[0]);
```

---

### Functions

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

**Objects** are key-value pairs

Note: If you are familiar with other programming languages, JavaScript objects are a bit different. You do not need to create classes in order to create objects.

The syntax to declare an object is:

```js
const object_name = {
  key1: value1,
  key2: value2,
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

###
