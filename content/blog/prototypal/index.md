---
title: Class & Prototypal Inheritance
date: "2020-03-25T19:45:00.000Z"
description: "Exploring the world of closures"
---

### What is the difference between the `var` and `let` keywords?

They do work very similarly, but the biggest different is their rules in regards to scope. 

The `var` keyword is hoisted to the top of the function in which it is called. Therefore, it can find itself in different locations. 

The `let` keyword on the otherhand is ___block scoped___. Meaning that the variable of a `let` keyword can only be accessed by those within its scope. 



```javascript
function Bear(type) {
    this.type = type;
}

var grizzly = new Bear('grizzly');
var black = new Bear('black');
var polar = new Bear('polar');

console.log(grizzly, black, polar);

```

## The Prototype Chain