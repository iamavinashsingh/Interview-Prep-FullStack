# Basic 

# Q1 :- What is JavaScript and how does it work in browsers?
- JavaScript is the language that handles the logic. It makes dead, static HTML pages alive, interactive, and dynamic.
- You use it to grab things on the screen and change them. For example, doing something when a user clicks a button:
```js
const button = document.getElementById('my-btn');
button.onclick = () => alert('You clicked me!');
```
- It’s the brain of the Frontend. And in the MERN stack, it’s the brain of the Backend too (Node.js). You basically write the whole app in one language.
- **JavaScript is the logic layer of the web that makes static HTML pages interactive and dynamic.**.

---

# Q2 :- Explain data types in JavaScript.
- JavaScript has two main buckets of data:
  - Simple stuff (Primitives): Text (strings), numbers, and true/false (booleans).
  - Complex stuff (Reference types): Objects (like a user profile) and Arrays (lists of things).
  ```js
  let age = 25;           // Simple (Number)
  let name = "PrepAce";   // Simple (String)
  let user = { id: 1 };   // Complex (Object)
  ```
- **JavaScript has simple primitive types like strings and numbers, and complex reference types like objects and arrays.**
---

# Q3 :- What is the difference between let, const, and var?
- Back in the day, we only had var. The problem? var ignores boundaries like if statements or for loops. It leaks out into the rest of your code, causing massive headaches when variables accidentally get overwritten.
- To fix this, JavaScript gave us let and const. They are "block-scoped," which just means they stay trapped inside the { } brackets where you put them. They don't leak.
  - Use let when the value is going to change later.
  - Use const when the value shouldn't be reassigned.
- *The biggest trap in interviews! People say const means the value can never change. Wrong. If const is an array or object, you can absolutely push new items into it or change its properties. You just can't reassign the whole variable using a new = sign.*


---

# Q4: Explain Hoisting in JavaScript

### What is Hoisting?

**Hoisting** in JavaScript means that during the **memory creation phase** (before code execution), JavaScript processes **variable and function declarations**.

> JavaScript remembers *names first*, assigns *values later*.


### Key Points (Interview-Oriented)

* JavaScript executes code in **two phases**:

  1. **Memory Creation Phase** – declarations are processed
  2. **Execution Phase** – code runs line by line
* Only **declarations** are hoisted, not assignments
* Hoisting behavior differs for `var`, `let`, `const`, and functions


## Function Hoisting (Easiest to Understand)

```js
sayHello();

function sayHello() {
  console.log("Hello!");
}
```

### What Happens?

* JavaScript already knows about `sayHello` before execution
* The function runs without any error

### Why?

* **Function declarations are fully hoisted** (both name and body)

**Interview Line:**

> Function declarations are hoisted completely, so they can be called before they are defined.



## Variable Hoisting with `var`

### Example

```js
console.log(a);
var a = 10;
```

### Output

```
undefined
```

### Why No Error?

Internally, JavaScript interprets the code like this:

```js
var a;        // declaration hoisted
console.log(a);
a = 10;       // assignment stays in place
```

### Important Notes

* Declaration is hoisted
* Assignment is **not** hoisted

**Interview Line:**

> Variables declared with `var` are hoisted and initialized with `undefined`.


## Variable Hoisting with `let` and `const` (Important)

### Example

```js
console.log(b);
let b = 20;
```

### Output

```
ReferenceError: Cannot access 'b' before initialization
```

### Are `let` and `const` Hoisted?

Yes — but **differently**:

* They are hoisted
* They are **not initialized**
* They exist in the **Temporal Dead Zone (TDZ)**



## Temporal Dead Zone (TDZ)

The time period between:

* Entering the scope
* And the actual declaration line

Accessing a variable in this zone causes a **ReferenceError**.

**Interview Line:**

> `let` and `const` are hoisted but remain in the Temporal Dead Zone until their declaration is evaluated.

---

# Q5 :- What are closures and how do they work?
