### 1. What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?

- getElementById returns only an element with the specified ID.
- getElementsByClassName returns an array-like object of all child elements of the specified ClassName.
- querySelector returns the first element of the specified css selector
  -querySelectorAll returns a static nodelist of all elements that match a CSS selector.

### 2. How do you create and insert a new element into the DOM?

- Get the container

```js
const container = document.getElementById("container");
```

- Create The element:

```js
const newElement = document.createElement("div");
```

- Set content

```js
newElement.innerHTML = "<h1>New Element</h1>";
```

- Insert new element into the DOM

```js
container.appendChild(newElement);
```

### 3. What is Event Bubbling and how does it work?

- In JavaScript, event bubbling occurs when you do something on a child element, such as clicking a button, automatically triggers the same event on its parent elements.
- Example:

```js
document.getElementById("child").addEventListener("click", function () {
  consol.log("child clicked");
}); 
document.getElementById("parent").addEventListener("click", function () {
  consol.log("parent clicked");
});
```
- Output
```consol
child clicked
parent clicked
```

### 4. What is Event Delegation in JavaScript? Why is it useful?
- Event Event delegation is a smart way to handle events. Instead of adding a listener to every similar element, you add one to the parent, and then use event.target to see which child element was interacted with.
- Event delegation is a useful pattern that allows you to write cleaner code and create fewer event listeners with similar logic.


### 5. What is the difference between preventDefault() and stopPropagation() methods?

- preventDefault Stops the browser from performing the default action for the event, such as following a link or submitting a form.

- Stops the event from bubbling up or being captured by the parent element.
