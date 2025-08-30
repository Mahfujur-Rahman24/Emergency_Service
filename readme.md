Answer 1:

The getElementById method selects only one element by its unique ID, while the getElementsByClassName method selects all elements with a given class name. The querySelector method selects the first element that matches a CSS selector, and the querySelectorAll method selects all elements that match a CSS selector.



Answer 2:
JavaScript for Creating and Inserting New Elements

• Step 1: Create the element: js.const newDiv = document.createElement("div").
• Step 2: Add content or attributes: js.newDiv.textContent = "Hello, I am new here!"; newDiv.className = "p-4 bg-blue-200 rounded";
• Step 3: Insert the element into the DOM: js.document.body.appendChild(newDiv);
• Step 4: Insert before another element: js.const target = document.getElementById("myElement"); document.body.insertBefore(newDiv, target);
• Step 5: Insert after another element: js.target.parentNode.insertBefore(newDiv, target.nextSibling);

Example: Adding a New List Item

• First: js.const li = document.createElement("li"); 
• Second: li.textContent = "Third item"; 
• Third: li.appendChild(li); 


Answer 3:

Definition:
Event Bubbling is the process where an event that occurs on a child element is first handled by that element, and then bubbles up through its ancestors in the DOM tree until it reaches the document object, unless stopped explicitly.

 Nested elements like 'Child Me' have click event listeners attached.
• Click event triggers on the button (child), bubbles up to its parent (div#parent), and continues bubbling up the DOM until reaching the top (document).
• If event propagates to parent elements, event.stopPropagation() can be used.
• Clicking the button only logs 'Child clicked', and the parent's event doesn't fire.

Answer 4:

Definition:

Event Delegation is a technique in JavaScript where you attach a single event listener to a parent element to handle events on its child elements, instead of attaching separate listeners to each child.
It works because of event bubbling—events on child elements bubble up to their parent, allowing the parent to detect them.

How it works:

When a <li> is clicked, the click event bubbles up to the <ul>.
The <ul> listener checks event.target to see which child was clicked.
The listener reacts accordingly.

Event delegation is beneficial for efficiency, dynamic elements, and simplified code, as it reduces repetitive code and memory usage by attaching only one listener to the parent element.

Answer 5:
The JavaScript functions `preventDefault()` and `stopPropagation()` have different purposes. `preventDefault()` prevents the default action of an element, which usually happens automatically. It prevents the event from bubbling up or capturing down the DOM, but does not prevent the default action. `stopPropagation()` stops the event from reaching other elements, but does not prevent the default action. Both functions are used in common use cases, such as link navigation and form submission, to prevent parent handlers from firing.
