# Assignment-5
1.What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?
Answer: 
The getElementById(id) method selects a single element using its unique ID,  getElementsByClassName(className) returns all elements that share the same class. The querySelector(selector) method selects the first element that matches a given CSS selector (ID, class, or tag), whereas querySelectorAll(selector) returns all matching elements as a NodeList, which behaves somewhat like an array.

2.How do you create and insert a new element into the DOM?
Answer:To add a new element to the DOM first use document.createElement() to make the element, then use appendChild() to place it inside the page wherever we want.

3.What is Event Bubbling and how does it work?
Answer:Event bubbling means that when we interact with an element like clicking a button the event first happens on that element and then travels upward to its parent elements.

For example:

<div id="parent">
  <button id="child">Click Me</button>
</div>

document.getElementById("parent").addEventListener("click", () => {
  console.log("Parent clicked!");
});

document.getElementById("child").addEventListener("click", () => {
  console.log("Child clicked!");
});


If we click the button, the browser will first log “Child clicked!” because the button is the target. After that, the event moves up to the parent <div> so we’ll see “Parent clicked!”.        

4.What is Event Delegation in JavaScript? Why is it useful?
Answer:  Event delegation in JavaScript is a technique where instead of adding a separate listener to each child we can attach a single event listener to a parent element to handle events on its child elements.
Example: <ul id="myList"> <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            </ul>
5.What is the difference between preventDefault() and stopPropagation() methods?
Answer: preventDefault() method is used in Java script to prevent default action that the browser would normally on the other hand stopPropagation() method is used in Java script to prevent the event from bubbling up the DOM tree.
