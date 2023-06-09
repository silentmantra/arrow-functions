My preferences about arrow functions are the following:
 * use them as an anonymous function where we don't need `this` 
 * use them when we need an outer scope's `this`
 * use them when a function's scope is small for example when it's used in the next lines
 * use them when a function is very small like an one-liner.

What I don't like very much is what I call **function spaghetti code** where logic and function definitions are mixed together.

Unfortunately arrow functions encourage this style of code and I don't like that.

And what I like in a usual `function` is that it's hoisted. So we can cleanly separate our logic from functions:

```
// some file/module/block

const start = step('start);

// some logic that uses our functions

// finish logic (could be even `return` statement)
// and start functions' definitions
// NO ANY OTHER CODE THAN FUNCTION DEFINITIONS BELOW

function step(){
 ...
}

function helper(){
 ...
}

```
