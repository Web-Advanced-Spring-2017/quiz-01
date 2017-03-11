# Quiz-01
**03-09-17**
*Time Limit 20min*
	
**Q1:** 

```
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

**Answer:**

**Q2:** 

```
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

**Answer:**




**Q3:** 

```
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

**Answer:**


**Q4:** 
What is the correct syntax for referring to an external script called "xxx.js"? (1 point)

1. `<script name="xxx.js">`
2. `<script src="xxx.js">`
3. `<script href="xxx.js">`

**Answer:**

**Q5:**

```
function whatDoesItDo(val){
	return val ? 1 : 2
}
```

1. It returns val
2. It always returns 2
3. It returns 1 if val is truthful, otherwise 2

**Answer:**


**Q6:**

```
function whatDoesItDo(num){
 return Math.max(0, Math.min(10, num))
}
```
1. Checks whether the number is between 0 and 10
2. Fits the number passed as a parameter in an interval from 0 to 10
3. Always returns 0

**Answer:**



**Q7:** 

```
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

**Answer:**


**Q8:** 
What does CSS stand for?
1. Colorful Style Symbols
2. Cascading Style Sheets
3. Computer State Secrets

**Q9:** 

```
var c = multiply(3,4)
console.log(c)

function multiply(a, b){
	a * b
}
```
The code above prints undefined in console. Why?
1. Trick question. It does print 12
2. Write your own solution on the right side

**Answer:**
 
**Q10:** 
What are the identifiers called that cannot be used as variables or function names?
1.  Reserved Words
2.  Constants
3.  Concrete Terms
4.  Favorites

**Q11:** 
What is a block of code called that is used to perform a specific task?
1.  Variable
2.  Declaration
3.  String
4.  Function

**Q12:** 
What is the element called that forms a search pattern out of a sequence of characters?
1.  RegExp or Regular Expression
2.  Boolean Variable
3.  Conditional Argument
4.  Event

**Q13:** 
Write a script that prints a multiple of 5 every 200ms, up to 50.














**Q14:** 
What is the difference between GET & POST Request






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
