## Answers 

### 1. What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?
=> getElementById() selects a single element using its unique ID and returns one Element object.
=> getElementsByClassName() selects multiple elements using a class name and returns a live HTMLCollection that     updates automatically when the DOM changes.
=>querySelector() selects the first element that matches any CSS selector,
=>querySelectorAll() selects all matching elements and returns a static NodeList that does not update automatically.


### 2. How do you create and insert a new element into the DOM?

=>Create a new element using document.createElement() and insert it into the DOM using methods like appendChild() or append().
exm:-const ul = document.querySelector("ul"); const li = document.createElement("li"); li.textContent = "Item 1"; ul.prepend(li);

### 3. What is Event Bubbling? And how does it work?
=>Event Bubbling is a process where an event starts from the target element and propagates upward through its parent elements in the DOM hierarchy.
When an event (like a click) occurs on a child element, it first runs on that element, then moves to its parent, then grandparent, and continues up to the document object. This allows parent elements to handle events triggered by their children.

### 4. What is Event Delegation in JavaScript? Why is it useful?
=>Event Delegation is a technique in JavaScript where a single event listener is attached to a parent element instead of multiple child elements. It works by using event bubbling, where the event moves from the child to the parent. The parent can detect which child triggered the event using event.target.
It is useful because it improves performance by reducing the number of event listeners, saves memory, and automatically works for dynamically added elements. This makes code cleaner and more efficient.


### 5. What is the difference between preventDefault() and stopPropagation() methods?
=> preventDefault() stops the browser’s default action for an event, such as preventing a form from submitting or a link from navigating to another page.
=>stopPropagation() stops the event from bubbling up the DOM tree, meaning parent elements will not receive the event.

=>In short, preventDefault() controls the browser’s behavior, while stopPropagation() controls event flow in the DOM.

