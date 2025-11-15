### Summary: Introduction to ES6 (ECMAScript 2015)

#### 1. What is ES6?
*   **ES6** (ECMAScript 6) is a major update to the JavaScript language specification, released in 2015.
*   It introduced powerful new features that changed how developers write JavaScript.
*   Newer versions are now named after their release year (e.g., ES2020).

#### 2. Key ES6 Features

##### `let` and `const`
*   **`let`**: Declares variables with **block scope**, preventing access outside the `{}` they are declared in. This solves issues with `var`, which has global scope.
*   **`const`**: Declares **constants** whose values cannot be reassigned after their initial definition.

##### Arrow Functions
*   A shorter and cleaner syntax for writing functions.
*   They are often used by assigning them to variables declared with `let` or `const`.
*   **Syntax Variations:**
    *   No parameters: `() => expression`
    *   One parameter: `param => expression` (parentheses are optional)
    *   Multiple parameters: `(param1, param2) => expression`
    *   Function body with multiple lines or a return value requires curly braces `{}`.

##### Promises
*   An object that represents the eventual completion (or failure) of an **asynchronous operation**.
*   **States:** A promise starts as **pending**, then becomes either **fulfilled** (success) or **rejected** (failure).
*   It uses `resolve` and `reject` callbacks to handle these outcomes.

##### Classes
*   Introduced a template for creating objects using a familiar class-based syntax, enabling **Object-Oriented Programming** in JavaScript.
*   **Key Concepts:**
    *   `constructor`: A special method for creating and initializing an object created with a class.
    *   `this`: Refers to the current instance of the class.
    *   `new` keyword: Used to create a new object instance from a class.
    *   **Inheritance:** A class (subclass) can inherit from another class (superclass) using the `extends` keyword and the `super()` method to call the parent constructor.
