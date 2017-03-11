# Quiz-01
**03-09-17**

*Time Limit: 20min*
	
**Q1:** 

```js
function() {
	var a = 10
	if (a > 5) {
		a = 7
	}
	alert(a)
}
```
When executed, what value will be alerted to the screen? Why?

1. 7
2. 10
3. null
4. undefined

**Answer: 1.**

First the variable `a` is initialized with value `10`. Then the code checks `if (a > 5)`, which is `true`. Therefore, it assigns `a` the value `7`. This later gets alearted on screen.

---

**Q2:** 

```js
function() {
	if(true) {
		var a = 5
	}
	alert(a)
}
```

When executed, what value will be alerted to the screen? Explain.

1. 0
2. 5
3. null
4. undefined

*Hint: Javascript has "Function Scope," as opposed to "Block Scope."*

**Answer: 2.**
One may think that `var a` cannot be accessed outside of the scope of `if(clause){ scope }` and the output should be `undefined`. However, the scope of a variable is extended to the `function()`, unlike many other languages, that won't allow you to access `a` outside of `if` statement. If that was the case with JavaSript, the output would have been `undefined`

---

**Q3:** 

```js
var a = 5
function first() {
	a = 6
}

function second() {
	alert(a)
}
```

Assuming I call these functions in order, what value gets alerted and why?

1. 0
2. 5
3. 6
4. null
5. undefined

**Answer: 3.**
`var a` is a global variable. The `first()` function runs first and modifies the global value of `a` to `6`. When the `second()` function runs after that, the new updated value `6` gets alearted.

---

**Q4:** 
What is the correct syntax for referring to an external script called "xxx.js"? (1 point)

1. `<script name="xxx.js">`
2. `<script src="xxx.js">`
3. `<script href="xxx.js">`

**Answer: 2.**
Following is the correct syntax. Refer to documentation [here](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script)

```html
<!-- HTML4 and (x)HTML -->
<script type="text/javascript" src="javascript.js"></script>

<!-- HTML5 -->
<script src="javascript.js"></script>
```

---

**Q5:**

```js
function whatDoesItDo(val){
	return val ? 1 : 2
}
```

1. It returns val
2. It always returns 2
3. It returns 1 if val is truthful, otherwise 2

**Answer: 3.**
`condition ? expr1 : expr2 ` is also known as [Conditional (ternary) Operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator). It can be unpacked into following code:

```js
function whatDoesItDo(val){
	if(val){
		return 1
	}else{
		return 2
	}
}

console.log(whatDoesItDo('test')) // Output: 1
console.log(whatDoesItDo())	// Output: 2
```

---

**Q6:**

```js
function whatDoesItDo(num){
 return Math.max(0, Math.min(10, num))
}
```

1. Checks whether the number is between 0 and 10
2. Fits the number passed as a parameter in an interval from 0 to 10
3. Always returns 0

**Answer: 2.**
- *Step:1* First, it takes in the value of `num` and evaluates the innermost function `Math.min(10,num)`. It finds out the smallest of the two values `10` and `num`. Let's call it `X` for now
- *Step:2* Now, it evaluates `Math.max(0, X)`. This returns the larger of the two values `0` and `X`
- In short, `step:1` caps the output to less than 10, then `step:2` caps the output to above `0`

```js
function whatDoesItDo(num){
 return Math.max(0, Math.min(10, num))
}

console.log(whatDoesItDo(5))	// Output: 5
console.log(whatDoesItDo(20))	// Output Max Range: 10
console.log(whatDoesItDo(-20))	// Output Min Range: 0
```

This function can be unpacked into following:

```js
function whatDoesItDo(num){
	var a = Math.min(10, num)
	b = Math.max(0,a)
	return b
}
```

---

**Q7:** 

```js
function whatDoesItDo(){
	var values = []
	myBlock: {
		values.push('1')
		values.push('2')
		break myBlock
		values.push('3')
	}
	values.push('4')
	return values.join(',')
}
```

1. It will return the string ‘1,2,3,4’
2. This is not valid JavaScript – it will throw an error
3. It will return the string ‘1,2,4’

**Answer: 3.**

- First, the code creates an empty array `var values = []` called 'values'. Next, it appends/pushes `'1'` to the array. `values = ['1']`
- Then `'2'` is pushed to the array. `values = ['1','2']`
- Now `break myBlock` prevents the execution of any following statements after itself, inside `myBlock:{ }`. So, `values.push('3')` never gets executed.
- Lastly, `values.push('4')`, pushed `'4'` to the array. `values = ['1','2','4']`
- `values.join(',')` returns a single string by concatenating all the values in the array `values[]`, seperated by the `,` symbol
- So the output is `1,2,4`

---

**Q8:** 
What does CSS stand for?

1. Colorful Style Symbols
2. Cascading Style Sheets
3. Computer State Secrets

**Answer: 2.**

---

**Q9:** 

```js
var c = multiply(3,4)
console.log(c)

function multiply(a, b){
	a * b
}
```
The code above prints undefined in console. Why?

1. Trick question. It does print 12
2. Write your own solution on the right side

**Answer: 2.**
The function does not `return` any value upon execution. Hence, when `var c = multiply(3,4)` gets executed, `multiply(3,4)` does not return `12` as expected, and no value gets assigned to `var c`. Correct solution is:

```js
var c = multiply(3,4)
console.log(c)

function multiply(a, b){
	return	a * b 	// Return a times b 
}
```
---

**Q10:** 
What are the identifiers called that cannot be used as variables or function names?

1.  Reserved Words
2.  Constants
3.  Concrete Terms
4.  Favorites

**Answer: 1.**
Here is a list of [reserved keywords](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Keywords) in ECMAScript 2015 

---

**Q11:** 
What is a block of code called that is used to perform a specific task?

1.  Variable
2.  Declaration
3.  String
4.  Function

**Answer: 4.**
"A function is a code snippet that can be called by other code or by itself, or a variable that refers to the function. When a function is called, arguments are passed to the function as input, and the function can optionally return an output. A function in JavaScript is also an object."
[Reference](https://developer.mozilla.org/en-US/docs/Glossary/Function)

---

**Q12:** 
What is the element called that forms a search pattern out of a sequence of characters?

1.  RegExp or Regular Expression
2.  Boolean Variable
3.  Conditional Argument
4.  Event

**Answer: 1.**
"Regular expressions are patterns used to match character combinations in strings. In JavaScript, regular expressions are also objects."
[Reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)

**Q13:** 
Write a script that prints a multiple of 5 every 200ms, up to 50.

**Answer:**

```js
var multiple = 0 // Start with initial value = 0.

var printMultiple = setInterval(function() {
	multiple += 5		// Add 5 to the current multiple value
	console.log(multiple)	// Print the multiple
	
	if (multiple === 50){						// When multiple is 50 
		clearInterval(printMultiple)	// Stop the printMultiple Interval
	}

}, 200)	// 200 ms interval 
```

---

**Q14:** 
What is the difference between GET & POST Request

**Answer:**
You may feel that `GET` requests data from server and `POST` sends data to server. That would be incorrect.
Both are HTTP requests that a client makes to the Server. 

![img](https://developer.mozilla.org/files/4291/client-server.png)

The web is based on a very basic client/server architecture that can be summarized as follows: a client (usually a Web browser) sends a request to a server (most of the time a web server like Apache, Nginx, IIS, Tomcat, etc.), using the HTTP protocol. The server answers the request using the same protocol.

**GET METHOD**

The GET method is the method used by the browser to ask the server to send back a given resource: "Hey server, I want to get this resource." In this case, the browser sends an empty body. Because the body is empty, if a form is sent using this method the data sent to the server is appended to the URL.

**POST METHOD**
The POST method is a little different. It's the method the browser uses to talk to the server when asking for a response that takes into account the data provided in the body of the HTTP request: "Hey server, take a look at this data and send me back an appropriate result." If a form is sent using this method, the data is appended to the body of the HTTP request.

**Must Read This Reference** : [Sending and Receiving Form Data](https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/Sending_and_retrieving_form_data)

**Q15:** 
Console Log:

```
module.js:442
		throw err;
		^

Error: Cannot find module 'gulp-sass'
		at Function.Module._resolveFilename (module.js:440:15)
		at Function.Module._load (module.js:388:25)
		at Module.require (module.js:468:17)
		at require (internal/module.js:20:19)
		at Object.<anonymous> (D:\WIP\gulpfile.js:4:12)
		at Module._compile (module.js:541:32)
		at Object.Module._extensions..js (module.js:550:10)
		at Module.load (module.js:458:32)
		at tryModuleLoad (module.js:417:12)
		at Function.Module._load (module.js:409:3)
```
Why is the error being generated in console. How can you fix it?

**Answer:**
The error is being thrown because the `gulp-sass` module that is required to execute the script is missing. You need to ensure that the module is within `node_modules` folder. If not, run `npm install gulp-sass --save`