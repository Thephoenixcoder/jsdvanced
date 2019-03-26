# jsdvanced

Function declartion   
#Hoisting

When a JavaScript file (or HTML document with JavaScript in it) is loaded, function declarations are hoisted to the top of the code by the browser before any code is executed.

what does that meaan ? 
Specifically, all of the functions written with function declarations are “known” before any code is run. This allows you to call a function before you declare.

/**
 * This works!
 */
function add(num1, num2) {
	return num1 + num2;
}
add(3, 3); // returns 6


/**
 * This does, too!
 */
substract(7, 4); // returns 3
function subtract(num1, num2) {
	return num1 - num2;
}

Function expression :

Function expressions, however, do not hoist. If you try to run a function before you’ve expressed it, you’ll get an error.

/**
 * This works!
 */
var add = function(num1, num2) {
	return num1 + num2;
};
add(3, 3); // returns 6


/**
 * This does not =(
 */
substract(7, 4); // returns Uncaught TypeError: subtract is not a function
var subtract = function (num1, num2) {
	return num1 - num2;
};


