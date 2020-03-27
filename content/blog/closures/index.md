---
title: Closure
date: "2020-03-25T19:45:00.000Z"
description: "Exploring the world of closures"
---

# Closures
Kyle Simpson mentions that closures in JavaScript are almost this elusive concept. Something magical that once a JavaScript developer gets it, they've reached JavaScript Nirvana. However, most all JavaScript developers use closure in their applications without even realizing it. It is one of those things that is so engrained in how JavaScript works, that developers have essentially taken it for granted. 

__So what is closure?__

Mozilla defines closure as: 
 > ...the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function’s scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time.

To put it in layman's terms, ___closure___ ensures that a function will always have access to variables defined __outside__ of its own ___lexical scope___. This access will be determined by the location the function is called. 

```javascript
// JavaScript Closure in its Most Basic Form
```