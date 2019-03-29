# jsadvanced

Function declartion  vs Function expression

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

Function expression(Anonymus function ) :

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
/////////////////////////////////////////////////////

#local scope vs global scope# 

#local scope

local Variables declared within a JavaScript function, become LOCAL to the function.
Local variables have Function scope: They can only be accessed from within the function.

// code here can NOT use carName

function myFunction() {
  var carName = "Volvo";

  // code here CAN use carName

}

#global scope# 

A variable declared outside a function, becomes GLOBAL.
A global variable has global scope: All scripts and functions on a web page can access it. 

var carName = "Volvo";

// code here can use carName

function myFunction() {

  // code here can also use carName 

}

/////////////////////
#To convert or treat declartion function to Expression function 

IFEE Pattern  --> Imediateley invoked fucntion  expression  

// Variation 1
(function() {
    alert("I am an IIFE!");
}());

// Variation 2
(function() {
    alert("I am an IIFE, too!");
})();
/////////
#BLOCK SCOPE VS FUNCTION SCOPE 
var --> scope function  
Let (es6+) --> between  {}
function foo() {
    // function scope
    if (condition) {
        // block scope
    }
}
//////////////////////////
Hoisting : 
 is Declaration variables and Declaration functions 
 var x ; 
 x=5 
------------
prototype :
all function inside 

----

==  ->  it is compare  value  
=== ->  it is compare value and type

---- 
object  linked 
===

high order function  
connect()(anotherfunction)
------
coercion 

it is like 

5==="5"   ==>  false 
5=="5"    ==> true 
---------

ternary operator 
----
stack  
first in first out 

----
let vs var 
let is block scope  
var  function scope 
----

let vs const 

const  cannot reaseigned  
const c=[1,2,3]
c=[3,4,5]  ==> it will  shut error can not assigned const value  

--
const c = [4,5,6]  
c.push(7)  it will successed  [4,5,6,7]
-----

different between  undefined  vs null 
both represent empty value 
if we used value  undefined  it will  be undefined  
if you use  null value  it will be object  
if you  define value and didnot assigned  it  js will create place holder name undefined 
---
convert json to  object  
var txt = '{"name":"John", "age":30, "city":"New York"}'
var obj = JSON.parse(txt);
convert object  to json 
var arr = [ "John", "Peter", "Sally", "Jane" ];
var myJSON = JSON.stringify(arr);
---

conviniet contact / 

