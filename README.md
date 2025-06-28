# JavaScript Cheatsheet M3S2: Your Quick Reference Guide

![JavaScript Cheatsheet](https://img.shields.io/badge/JavaScript-Cheatsheet-brightgreen.svg)

## Table of Contents

- [Overview](#overview)
- [Key Concepts](#key-concepts)
  - [APIs](#apis)
  - [Arrays](#arrays)
  - [Async/Await](#asyncawait)
  - [Callbacks](#callbacks)
  - [Classes](#classes)
  - [Closures](#closures)
  - [CRUD Operations](#crud-operations)
  - [DOM Manipulation](#dom-manipulation)
  - [Hoisting](#hoisting)
  - [Maps](#maps)
  - [Modules](#modules)
  - [Objects](#objects)
  - [Promises](#promises)
  - [Prototypes](#prototypes)
  - [Scope](#scope)
  - [Sets](#sets)
  - [The `this` Keyword](#this-keyword)
- [Download and Usage](#download-and-usage)
- [Contributing](#contributing)
- [License](#license)

## Overview

This repository contains a comprehensive JavaScript cheatsheet tailored for M3S2. It serves as a quick reference to help you review essential JavaScript concepts. Whether you are a beginner or an experienced developer, this cheatsheet can assist you in grasping important topics quickly.

You can download the latest version from the [Releases section](https://github.com/KasperShuvo/JavaScript-M3S2-Cheatsheet/releases). 

## Key Concepts

### APIs

APIs (Application Programming Interfaces) allow different software systems to communicate. JavaScript often interacts with APIs to fetch or send data. Here are key points:

- **Fetch API**: Use `fetch()` to make network requests.
- **REST APIs**: Follow REST principles for resource management.
- **JSON**: JavaScript Object Notation is the standard data format.

### Arrays

Arrays are used to store multiple values in a single variable. Key methods include:

- **Push**: Adds an item to the end.
- **Pop**: Removes the last item.
- **Shift**: Removes the first item.
- **Unshift**: Adds an item to the beginning.
- **Map**: Creates a new array with results of calling a function on every element.

### Async/Await

Async/await is a modern way to handle asynchronous code. It makes your code cleaner and easier to read. Example:

```javascript
async function fetchData() {
    let response = await fetch('https://api.example.com/data');
    let data = await response.json();
    console.log(data);
}
```

### Callbacks

A callback is a function passed into another function as an argument. They are often used for asynchronous operations. Example:

```javascript
function fetchData(callback) {
    setTimeout(() => {
        callback("Data fetched");
    }, 1000);
}

fetchData(data => console.log(data));
```

### Classes

Classes are a way to create objects in JavaScript. They allow for inheritance and encapsulation. Example:

```javascript
class Animal {
    constructor(name) {
        this.name = name;
    }
    speak() {
        console.log(`${this.name} makes a noise.`);
    }
}

let dog = new Animal('Dog');
dog.speak();
```

### Closures

A closure is a function that retains access to its lexical scope, even when the function is executed outside that scope. Example:

```javascript
function outer() {
    let count = 0;
    return function inner() {
        count++;
        console.log(count);
    };
}

let increment = outer();
increment(); // 1
increment(); // 2
```

### CRUD Operations

CRUD stands for Create, Read, Update, and Delete. These are the four basic operations for managing data. In JavaScript, you can perform these operations using APIs or databases.

- **Create**: Use POST requests to add new data.
- **Read**: Use GET requests to retrieve data.
- **Update**: Use PUT or PATCH requests to modify existing data.
- **Delete**: Use DELETE requests to remove data.

### DOM Manipulation

The Document Object Model (DOM) represents the structure of a webpage. JavaScript can manipulate the DOM to change the content, structure, and style of a webpage.

- **Select Elements**: Use `document.getElementById()` or `document.querySelector()`.
- **Change Content**: Use `element.textContent` or `element.innerHTML`.
- **Add Event Listeners**: Use `element.addEventListener()`.

### Hoisting

Hoisting is JavaScript's default behavior of moving declarations to the top of the current scope. Variables declared with `var` are hoisted, while `let` and `const` are not.

### Maps

Maps are collections of key-value pairs. They maintain the insertion order of keys. Example:

```javascript
let map = new Map();
map.set('key1', 'value1');
map.set('key2', 'value2');
console.log(map.get('key1')); // value1
```

### Modules

Modules allow you to break your code into separate files. You can export and import functions, objects, or variables. Example:

**In `module.js`:**

```javascript
export function greet(name) {
    return `Hello, ${name}!`;
}
```

**In `main.js`:**

```javascript
import { greet } from './module.js';
console.log(greet('World'));
```

### Objects

Objects are collections of properties. Each property is a key-value pair. Example:

```javascript
let person = {
    name: 'Alice',
    age: 25,
    greet: function() {
        console.log(`Hello, my name is ${this.name}`);
    }
};

person.greet(); // Hello, my name is Alice
```

### Promises

Promises are objects that represent the eventual completion or failure of an asynchronous operation. Example:

```javascript
let promise = new Promise((resolve, reject) => {
    setTimeout(() => {
        resolve("Success!");
    }, 1000);
});

promise.then(result => console.log(result));
```

### Prototypes

Every JavaScript object has a prototype. Prototypes allow you to add properties and methods to existing objects. Example:

```javascript
function Person(name) {
    this.name = name;
}

Person.prototype.greet = function() {
    console.log(`Hello, my name is ${this.name}`);
};

let alice = new Person('Alice');
alice.greet(); // Hello, my name is Alice
```

### Scope

Scope defines the visibility of variables. There are three types:

- **Global Scope**: Variables declared outside any function.
- **Function Scope**: Variables declared within a function.
- **Block Scope**: Variables declared with `let` or `const` within a block.

### Sets

Sets are collections of unique values. They can hold any type of value. Example:

```javascript
let set = new Set();
set.add(1);
set.add(2);
set.add(1); // Will not be added again
console.log(set.size); // 2
```

### The `this` Keyword

The `this` keyword refers to the object it belongs to. Its value can change based on how a function is called. Example:

```javascript
let obj = {
    name: 'Alice',
    greet: function() {
        console.log(`Hello, ${this.name}`);
    }
};

obj.greet(); // Hello, Alice
```

## Download and Usage

To get started, download the latest version of the cheatsheet from the [Releases section](https://github.com/KasperShuvo/JavaScript-M3S2-Cheatsheet/releases). Follow the instructions provided in the release notes to set up and use the cheatsheet effectively.

## Contributing

We welcome contributions to improve this cheatsheet. If you would like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Submit a pull request.

Please ensure your code adheres to the existing style and conventions.

## License

This project is licensed under the MIT License. Feel free to use and modify it as needed.