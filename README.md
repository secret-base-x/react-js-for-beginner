# How to get job as a react developer for beginner

## Sponsorship

Support me at [Ko-fi](https://ko-fi.com/secretbasex)

## Useful mental model for learning

### Top down learning technique

The top-down learning approach is a method of learning where the learner starts with a general understanding of a concept and then breaks it down into smaller, more specific components. This method is also known as "deductive learning" because the learner is presented with a general idea or rule and then deduces specific examples or applications of that rule.

It would be overwhelming to try to understand every detail all at once. A better approach would be to first learn the frequently used patterns and their corresponding outputs, without fully understanding them. Once you have a grasp of these patterns, you can then dive deeper into the details and gain a better understanding of the material.

You can learn about top down learning approch here

[![Blackbox Techniques](https://img.youtube.com/vi/RDzsrmMl48I/0.jpg)](https://www.youtube.com/watch?v=RDzsrmMl48I)

### 20 Mile March

The "20 Mile March" mental model is a concept popularized by Jim Collins in his book "Great by Choice." It refers to the idea that consistent progress towards a goal, even if it is slow, is more likely to lead to success than sporadic bursts of activity. The metaphor of a march refers to a steady, consistent pace that is maintained over a long period of time. The idea is to set a minimum threshold for progress and then consistently hit that threshold, rather than trying to exceed it every day. This approach helps to mitigate the risks associated with unpredictability and helps to ensure that progress is being made towards a goal even when faced with adversity.

## Functional Programming 

### Filtering

When working with business applications, we often receive data in the form of an array of objects and want to filter it based on certain properties. In this example, we have an array of product objects with properties such as name, price, and category. We want to filter the products and only get those in the "Electronics" category and with a price below $800.

```javascript
const products = [
    {id: 1, name: "Laptop", price: 800, category: "Electronics"},
    {id: 2, name: "Tablet", price: 300, category: "Electronics"},
    {id: 3, name: "Camera", price: 600, category: "Photography"},
    {id: 4, name: "Shirt", price: 50, category: "Clothing"},
    {id: 5, name: "Pants", price: 70, category: "Clothing"}
];

const filteredProducts = products.filter(product => product.category === "Electronics" && product.price < 800);
console.log(filteredProducts); 
// Output: [{name: "Tablet", price: 300, category: "Electronics"}]
```

## Common patterns in React for business applications
In real-world business applications, there are many commonly used patterns in React that repeat frequently. For beginners, it is beneficial to study these patterns as it can aid in understanding how they work and the subtle details involved. Even if the patterns are not fully understood at first, by studying multiple patterns, an individual will be able to gain a deeper understanding over time.

### Toggle Visibility

In React, you can use state to toggle the visibility of an item. Here is an example of how you can do this:
u
```javascript
import React, { useState } from 'react';

function App() {
  const [isVisible, setIsVisible] = useState(true);

  const toggleVisibility = () => {
    setIsVisible(!isVisible);
  }

  return (
    <div>
      <button onClick={toggleVisibility}>Toggle Visibility</button>
      {isVisible && <p>This is some visible text.</p>}
    </div>
  );
}

export default App;
```
In this example, a button element is rendered with an onClick event listener that calls the toggleVisibility function. The toggleVisibility function toggles the value of the isVisible state variable between true and false. If isVisible is true, the p element is rendered, otherwise it will not be rendered.

You can apply this logic to your item that you want to toggle visibility.

#### Encapsulate the toggle login into custom hook useToggle

```javascript
import { useState } from 'react';

function useToggle(initialValue) {
  const [value, setValue] = useState(initialValue);
  
  const toggle = () => {
    setValue(!value);
  };
  
  return [value, toggle];
}

export default useToggle;
```

You can then use useToggle like this

```javascript
import React from 'react';
import useToggle from './useToggle';

function App() {
  const [isVisible, toggleVisibility] = useToggle(true);

  return (
    <div>
      <button onClick={toggleVisibility}>Toggle Visibility</button>
      {isVisible && <p>This is some visible text.</p>}
    </div>
  );
}

export default MyComponent;
```
