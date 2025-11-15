# Introduction

## React
 - creating an in-memory virtual DOM rather than directly manipulating the browser’s DOM. 
 - performs necessary manipulations within this virtual representation before applying changes to the actual browser DOM.


## Here’s how the process works:

# 1. Actual DOM and Virtual DOM

<img width="1000" height="500" alt="image" src="https://github.com/user-attachments/assets/b4c811b0-f75f-4c72-af35-5a5e8436e7cc" />


- Initially, there is an Actual DOM(Real DOM) containing a div with two child elements: h1 and h2.
React maintains a previous Virtual DOM to track the UI state before any updates.
2. Detecting Changes

- When a change occurs (e.g., adding a new h3 element), React generates a New Virtual DOM.
React compares the previous Virtual DOM with the New Virtual DOM using a process called reconciliation.
3. Efficient DOM Update

- React identifies the differences (in this case, the new h3 element).
Instead of updating the entire DOM, React updates only the changed part in the New Actual DOM, making the update process more efficient.


### 1. Libraries vs. Frameworks
*   **Library:** A collection of prewritten, reusable code for specific tasks (e.g., jQuery, Lodash, React). You call functions from a library in your code.
*   **Framework:** A comprehensive platform that provides the foundation and structure for building entire applications (e.g., AngularJS, Vue.js). It imposes an architecture, and your code fits into the framework.

### 2. Front-end Frameworks
*   A specialized type of framework focused on building the **user-facing side** of web applications.
*   They use HTML, CSS, and JavaScript to create dynamic and interactive user interfaces (UIs).
*   Popular examples include **React, AngularJS, and Vue.js**.

### 3. Introduction to React
*   React is an **open-source JavaScript library** developed by Meta (Facebook) for building dynamic and interactive user interfaces.

### 4. Prominent Features of React
*   **Component-Based Architecture:** UIs are built from independent, reusable components (e.g., header, sidebar).
*   **Declarative Syntax:** You describe *what* the UI should look like for a given state, and React handles updating the DOM to match that description.
*   **Virtual DOM:** React creates a virtual representation of the DOM. When changes occur, it compares this virtual DOM with the real DOM and updates only the necessary parts, improving performance.
*   **One-Way Data Binding:** Data flows in one direction, from parent components to child components, simplifying data management and reducing bugs.
*   **JSX (JavaScript XML):** A syntax extension that allows you to write HTML-like code within JavaScript, making it easier to create and visualize UI components.
*   **Hooks:** A feature that allows developers to use state and other React features in function components, simplifying logic and promoting code reuse without class-based coding.



    *   `this`: Refers to the current instance of the class.
    *   `new` keyword: Used to create a new object instance from a class.
    *   **Inheritance:** A class (subclass) can inherit from another class (superclass) using the `extends` keyword and the `super()` method to call the parent constructor.
