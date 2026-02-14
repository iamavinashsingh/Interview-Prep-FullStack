# Basic 

## Q1 :- What is JavaScript and how does it work in browsers?
- JavaScript is the language that handles the logic. It makes dead, static HTML pages alive, interactive, and dynamic.
- You use it to grab things on the screen and change them. For example, doing something when a user clicks a button:
```js
const button = document.getElementById('my-btn');
button.onclick = () => alert('You clicked me!');
```
- It’s the brain of the Frontend. And in the MERN stack, it’s the brain of the Backend too (Node.js). You basically write the whole app in one language.
- **JavaScript is the logic layer of the web that makes static HTML pages interactive and dynamic.**.

---

## Q2 :- Explain data types in JavaScript.
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
