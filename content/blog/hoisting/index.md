---
title: Hoisting
date: "2020-03-25T19:45:00.000Z"
description: "Exploring the world of Hoisting"
---

```javascript
// Hoisting in JavaScript

function variableDeclarations() { 
   
  var messageOne; // Declaration
  messageOne = 'one'; // Initialization
  console.log(messageOne); // Returns 'one'

  messageTwo = 'two'; // No hoisting, but since initialization happens (and there is not declaration already), it also causes declaration
  console.log(messageTwo); // Returns 'two'
  
  messageThree = 'three'; // Initialization
  console.log(messageThree); // Returns 'three'
  var messageThree; // Declaration causes variable to be hoisted
  
  console.log(messageFour); // Returns undefined as it sees the hoisted variable, but the initialization happens after
  var messageFour; // Declaration
  messageFour = 'four'; // Initialization
  
  console.log(messageFive); // Returns undefined as it sees the hoisted variable, but the initialization happens after
  var messageFive = 'five'; // Delaration & Initialization
  
  // console.log(messageZ); // Throws Reference Error as it doesn't see any declaration and therefore doesn't know if the variable exists
  // messageZ = 'This is message Z'; // Only Initialization  
}

function functionDeclarations(){
  // Function declarations are hoisted to the top of their scope.

  function messageOne(message) {
    console.log('Message: ' + message );
  }
  
  messageOne('I am seemingly called AFTER my function\'s declaration. Will I show up in the console log?'); 
  messageTwo('I am seemingly called BEFORE my function\'s declaration. Will I show up in the console log?'); 
  // Both function calls show up in the console log because function declarations are hoisted to the top of their scope! 
  
  function messageTwo(message) {
    console.log('Message: ' + message );
  }
  
}

variableDeclarations();
functionDeclarations();```