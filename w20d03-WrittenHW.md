<h3>What are all the JavaScript Data Types?</h3>
String, Boolean, Number, Array, Object,

<h3>What is the Difference Between Const Let and Var? Consider Scope ... Give an example</h3>

Var is the old method of declaring a variable in JavaScript while Let and Const are the newer methods. The value of Let variables can be re-declared and updated while Const variables cannot. Also, both Let and Const cannot be assessed if they are both declared within a block scope. 


<h3>Pass By Value vs Pass By Reference? Why would you say a String is pass by value/ or a value type? Why is an object a reference type?</h3>
pass by value is when the value of the function parameter is copied into another location and when accessing or modifying the variable within the function, only the copy is accessed/modified and the origninal value remains the same. Pass by reference passes the original variable into the function parameter and the result will modify the original variable. 


<h3>What do Map , Filter and Reduce do? Do they mutate the array you call them on? </h3>

.map() takes a callback argument and runs for each value in the array and returns each new value in a new array.

.reduce() runs a callback but reduces the result from one array element to other and is an easy way to return a single value or object from an array. 

.filter() runs a callback and returns only that element as a new array 

<h3>What are all the Falsey Values in JavaScript? Why do you think this is important to know?</h3>

the number 0
the BigInt 0n
the keyword null
the keyword undefined
the boolean false
the number NaN
the empty string "" (equivalent to '' or `backticks`)

Falsey values are a way that JS deals with not crashing when a conditional is passed something other than a boolean value.

<h3>What are Async and Await?</h3>

Basically, async accompanies a function with will return a promise and await waits until that promise settles and returns the result 

<h3>What is an async function?</h3>

A async function returns a promise. 

<h3>What are try and catch?</h3>

The try and catch statement is compromised of a try block that will run the code inside of that block and if there are any errors, the catch block will catch that error and the code will throw an error.

