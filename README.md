React is a popular JavaScript library for building user interfaces, and one of the key features of React is its ability to manage state. In this article, we will explore how to build a simple counter application in React using the `useState` hook.

The `useState` hook is a built-in hook that allows us to add state to functional components. It takes one argument, the initial state, and returns an array with two elements: the current state and a function to update it. Here's an example of how to use `useState` to create a state variable called `count` with an initial value of 0:

```js
const [count, setCount] = useState(0);
```
In this example, the `count` variable holds the current value of the counter, and the `setCount` function is used to update the value of the counter.

Now that we have our state set up, we can use it to render the component. Here is the complete code for our counter component:


```js
import React, { useState } from 'react';
function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>{count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
      <button onClick={() => setCount(count - 1)}>Decrement</button>
    </div>
  );
}
export default Counter;
```
In this example, we render a `div` element that contains a `span` element displaying the current count, and two buttons that increment or decrement the count when clicked. The `onClick` handlers for the buttons call the `setCount` function, passing in the new count.

When the `setCount` function is called, React will re-render the component with the new count value. This allows us to easily update the component whenever the count changes.

One thing to note is that when the `setCount` function is called, it does not modify the original `count` variable, instead, it creates a new one with the new value. This is how React is able to track changes to the component and re-render it as needed.

In summary, the `useState` hook is a powerful tool for managing state in React functional components. It allows us to easily add state to our components and update it as needed, making it simple to build complex, interactive applications. The simple counter app is a great example of how easy it is to get started with `useState` and start building React applications.