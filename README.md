## Scope, hoisting and compartmentalization

### Answer the following:
In you own words, explain the concepts of scope, hoisting, compartmentalization.
Scope refers to how a javascript document is organized and what parts are accessible by others. Global scope is everything within the window and all functions have access to it. Local scope is the scope within a block of code and and only that block of code has access to it.

Hoisting is when javascript automatically declarations of variables and functions to the top of the file. However, the assignments are not hoisted.

Compartmentalization is used so that the global scope is not affected by every change the user makes. This is often accomplished by using IIFE's

### Provide examples for all three, below:

#### Scope:
var dog = "golden retriever";

function dogs(){
  var dog = "german shepard"
}
<!--  In this example the first var dog is in the global scope and the second var dog is in the local scope of the function dogs()-->


#### Hoisting:
function dogs(){
  var dog = "golden retriever";
}
In the above scenario the declaration of the var dog would be sent to the top of the page above the function.



#### Compartmentalization:
( function() {
  "use strict";
  const language = 'HTML';

  ( function styling() {
    const language = 'CSS'
    console.log( language );
    console.assert( language == "CSS", "Test Failed. Did you compartmentalize?" );
  } )();

  console.log( language );
  console.assert( language == "HTML", "Test Failed. Did you compartmentalize?" );
} )();

In the above scenario styling() is compartmentalized because it is within an IIFE so nothing else can access what is inside of it.




<!--  -->
