# How to get job as a react developer for beginner

## Sponsorship

Support me at [Ko-fi](https://ko-fi.com/secretbasex)

## Top down learning technique

The top-down learning approach is a method of learning where the learner starts with a general understanding of a concept and then breaks it down into smaller, more specific components. This method is also known as "deductive learning" because the learner is presented with a general idea or rule and then deduces specific examples or applications of that rule.

It would be overwhelming to try to understand every detail all at once. A better approach would be to first learn the frequently used patterns and their corresponding outputs, without fully understanding them. Once you have a grasp of these patterns, you can then dive deeper into the details and gain a better understanding of the material.

You can learn about top down learning approch here

[![Blackbox Techniques](https://img.youtube.com/vi/RDzsrmMl48I/0.jpg)](https://www.youtube.com/watch?v=RDzsrmMl48I)

## Functional Programming 

### Filtering

When working with business applications, we often receive data in the form of an array of objects and want to filter it based on certain properties. In this example, we have an array of product objects with properties such as name, price, and category. We want to filter the products and only get those in the "Electronics" category and with a price below $800.

```javascript
const products = [
    {name: "Laptop", price: 800, category: "Electronics"},
    {name: "Tablet", price: 300, category: "Electronics"},
    {name: "Camera", price: 600, category: "Photography"},
    {name: "Shirt", price: 50, category: "Clothing"},
    {name: "Pants", price: 70, category: "Clothing"}
];

const filteredProducts = products.filter(product => product.category === "Electronics" && product.price < 800);
console.log(filteredProducts); 
// Output: [{name: "Tablet", price: 300, category: "Electronics"}]
```
