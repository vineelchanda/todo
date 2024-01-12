Functions :  a function is a value.
A function is a value representing an “action”

----------------------------------------------

sayHi("John"); // Hello, John
// Function Declaration
function sayHi(name) {
  alert( `Hello, ${name}` );
}

------------------------------------------------

sayHi("John"); // error!
// Function Expression
let sayHi = function(name) {  // (*) no magic any more
  alert( `Hello, ${name}` );
};

-----------------------------------------------------

The more subtle difference is when a function is created by the JavaScript engine.

A Function Expression is created when the execution reaches it and is usable only from that moment.

Once the execution flow passes to the right side of the assignment let sum = function… – here we go, the function is created and can be used (assigned, called, etc. ) from now on.

Function Declarations are different.

A Function Declaration can be called earlier than it is defined.

For example, a global Function Declaration is visible in the whole script, no matter where it is.

That’s due to internal algorithms. When JavaScript prepares to run the script, it first looks for global Function Declarations in it and creates the functions. We can think of it as an “initialization stage”.


-----------------------------------------------------------------------------------


#function basics

if no return value is returned undefined is sent

default values are set if no values are given when function is called. if default values are not set, undefined is set

arguments object is available in function scope, which has all the arguments in order


###Arrow functions 
    are handy for simple actions, especially for one-liners. They come in two flavors:

Without curly braces: (...args) => expression – the right side is an expression: the function evaluates it and returns the result. Parentheses can be omitted, if there’s only a single argument, e.g. n => n*2.
With curly braces: (...args) => { body } – brackets allow us to write multiple statements inside the function, but we need an explicit return to return something.
