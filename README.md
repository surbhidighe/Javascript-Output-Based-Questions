# JavaScript output based interview questions 
---

#### Click :star: if you like it!!
Every contribution counts, regardless of its size. I value and appreciate the efforts of all contributors, from beginners to seasoned developers. Join me on this exciting journey of open-source collaboration. **Together, let's build something amazing!** :handshake:

--- 

#### Contribution Guidelines

- :point_right: Please ensure that your contributions adhere to the coding style and guidelines of this project
- :point_right: Include clear and concise commit messages for all your commits
- :point_right: Provide a detailed description of your changes in the pull request.
- :point_right: Be respectful and considerate towards other contributors.

---

**1. What will be the output**
```js
let arr = [1, 2, 3, 4, 5, -6, 7];
arr.length = 0;
console.log(arr);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : [ ]</li>
	<li><b>Reason</b> : The length of the array has been set to 0, so the array becomes empty.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**2. What will be the output**
```js
x = 10;
console.log(x);
var x;
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 10</li>
	<li><b>Reason</b> : The declaration of the variable x is hoisted to the top of its scope.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**3. What will be the output**
```js
let a = { x: 1, y: 2 }
let b = a;
b.x = 3;
console.log(a);
console.log(b);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : { x: 3, y: 2 } { x: 3, y: 2 }</li>
	<li><b>Reason</b> : 'a' and 'b' both are pointing to the same reference.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**4. What will be the output**
```js
for(var i = 0; i < 10; i++){
    setTimeout(function(){
      console.log("value is " + i);
  })
}
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 10 times, "value is 10"</li>
	<li><b>Reason</b> : "var" has a function scope, and there will be only one shared binding for the iterations. By the time the setTimeout function gets executed, the for loop has already completed and the value of the variable i is 10.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**5. What will be the output**
```js
for(let i = 0; i < 10; i++){
    setTimeout(function(){
      console.log("value is " + i);
  })
}
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 10 times "value is" followed by the value of i in each iteration, from 0 to 9</li>
	<li><b>Reason</b> : "let" has a block scope, and a new binding will be created for each iteration. Here, a new variable i is created and has a different value for each iteration of the loop.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**6. What will be the output**
```js
function hello() {
  console.log("1");
    setTimeout(() => {
        console.log("2");
    })
  console.log("3");
}
hello();
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : "1" followed by "3", and then after a small delay, "2"</li>
	<li><b>Reason</b> : console.log("1") statement logs "1" to the console. Then setTimeout() function is set to execute the callback function in the next event loop iteration and logs "3" to the console.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**7. What will be the output**
```js
let f = "8";
let a = 1;
console.log((+f)+a+1);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 10</li>
	<li><b>Reason</b> : The expression (+f) is a shorthand way to convert the string value of f to a number. Therefore, (+f) evaluates to 8.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**8. What will be the output**
```js
let a = 10;
if(true){
   let a = 20;
   console.log(a, "inside");
}
console.log(a, "outside");
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 20, "inside" and 10, "outside"</li>
	<li><b>Reason</b> : The variable "a" declared inside "if" has block scope and does not affect the value of the outer "a" variable.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**9. What will be the output**
```js
var a = "xyz";
var a = "pqr";
console.log(a)
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : "pqr"</li>
	<li><b>Reason</b> : Both the variables are declared using "var" keyword with the same name "a". The second variable declaration will override the first variable declaration.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**10. What will be the output**
```js
const arr1 = [1, 2, 3, 4];
const arr2 = [6, 7, 5];
const result = [...arr1, ...arr2];
console.log(result);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : [1, 2, 3, 4, 6, 7, 5]</li>
	<li><b>Reason</b> : Spread operator (...) concatenates the two arrays into "result" array.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**11. What will be the output**
```js
const person1 = { name: 'xyz', age: 21 };
const person2 = { city: 'abc', ...person1 };
console.log(person2);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : { city: 'abc', name: 'xyz', age: 21 }</li>
	<li><b>Reason</b> : Spread operator (...) copies all the properties from person1 into person2.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**12. What will be the output**
```js
console.log(5 < 6 < 7);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : true</li>
	<li><b>Reason</b> : In JavaScript, the < operator evaluates expressions from left to right. First, the expression 5 < 6 is evaluated, resulting in true because 5 is less than 6. Then, the expression true < 7 is evaluated. In this case, JavaScript performs type coercion and converts true to the number 1. Therefore, the expression becomes 1 < 7, which is true.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**13. What will be the output**
```js
console.log(7 > 6 > 5);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : false</li>
	<li><b>Reason</b> : In JavaScript, the > operator evaluates expressions from left to right. First, the expression 7 > 6 is evaluated, resulting in true because 7 is greater than 6. Then, the expression true > 5 is evaluated. In this case, JavaScript performs type coercion and converts true to the number 1. Therefore, the expression becomes 1 > 5, which is false.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**14. What will be the output**
```js
console.log(0 == false);
console.log(1 == true);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : true, true</li>
	<li><b>Reason</b> : The == operator converts operands to a common type before making the comparison. In both the cases, the boolean value will be converted to a number, i.e., false is converted to 0 and true is converted to 1. So, the expression 0 == false is equivalent to 0 == 0 and 1 == true is equivalent to 1 == 1.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**15. What will be the output**
```js
console.log([11, 2, 31] + [4, 5, 6]);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : "11,2,314,5,6"</li>
	<li><b>Reason</b> : The + operator is used for both addition and string concatenation. When you try to concatenate two arrays using the + operator, the arrays are converted to strings and then concatenated together. In this case, the arrays [11, 2, 31] and [4, 5, 6] are converted to strings as "11,2,31" and "4,5,6" respectively. Then, the two strings are concatenated, resulting in "11,2,314,5,6".</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**16. What will be the output**
```js
console.log({} == {}); 
console.log({} === {});
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : false, false</li>
	<li><b>Reason</b> : When you compare objects using == or ===, it checks if they refer to the exact same object. So even if they are looking same, they are pointing to different memory locations.</li>
</ul>
</details>
	
**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**17. What will be the output**
```js
let x = 5;
let y = x++;
console.log(y);
console.log(x)
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 5, 6</li>
	<li><b>Reason</b> : The post-increment operator increments and returns the value before incrementing.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**18. What will be the output**
```js
let x = 5;
let y = ++x;
console.log(y);
console.log(x)
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 6, 6</li>
	<li><b>Reason</b> : The pre-increment operator increments and returns the value after incrementing.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**19. What will be the output**
```js
console.log('apple'.split(''));
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : [ 'a', 'p', 'p', 'l', 'e' ]</li>
	<li><b>Reason</b> : split method is used to split a string into an array of substrings based on a specified separator. </li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**20. What will be the output**
```js
const arr = [2,3,5,2,8,10,5];
console.log(arr.indexOf(5))
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 2</li>
	<li><b>Reason</b> : indexOf method returns the index of the first occurrence of the specified element in the array. </li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**21. What will be the output**
```js
const array = [8, 18, 28, 38];
const result = array.map(element => element + 2)
               .filter((element) => element > 25);
console.log(result);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : [ 30, 40 ]</li>
	<li><b>Reason</b> : The code increments each element in the array by 2 using map and filters out elements greater than 25 using filter.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**22. What will be the output**
```js
function checkValue(value){
    var result = Array.isArray(value);
    console.log(result);
}
checkValue([1,2,3]);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : true</li>
	<li><b>Reason</b> : Array.isArray() method is used to check if the provided value is an array.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**23. What will be the output**
```js
function sum(a=5, b=7){
    return a+b;
}
console.log(sum(undefined, 20));
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 25</li>
	<li><b>Reason</b> : Here, undefined is passed as the value for parameter a, and 20 is passed for parameter b. When any parameter is undefined, the default value is used. </li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**24. What will be the output**
```js
console.log(10 + "5");
console.log("5" + 10);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 105, 510</li>
	<li><b>Reason</b> : Since one operand is a string, the + operator performs string concatenation. </li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**25. What will be the output**
```js
console.log(10 - "5");
console.log("5" - 10);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 5, -5</li>
	<li><b>Reason</b> : In JavaScript, when the subtraction operator - is used, the operands are converted to numbers before performing the subtraction </li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**26. What will be the output**
```js
console.log(printName());
function printName(){
    return "Hi my name is Bob"
}
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : Hi my name is Bob</li>
	<li><b>Reason</b> : Regular functions are hoisted to the top. And you can access and call them even before they are declared. </li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**


**27. What will be the output**
```js
console.log(printName());
const printName = () => {
    return "Hi my name is Bob"
}
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : ReferenceError: Cannot access 'printName' before initialization</li>
	<li><b>Reason</b> : Arrow functions cannot be accessed before they are initialised. </li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**1. What will be the output (shallow copy of an object)**
```js
const userDetails = {
  firstName: "Surbhi",
  lastName: "Dighe",
  age: 20,
  address: {
    city: "Hyderabad",
    country: "India",
  },
};

let cloneUserDetails = { ...userDetails };

//Updating original object
userDetails.age = 22;
userDetails.address.city = "Banglore";

console.log(cloneUserDetails.age); // what will be the output
console.log(cloneUserDetails.address.city); // what will be the output
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 20, "Banglore"</li>
	<li><b>Explanation </b> : cloneUserDetails is created by using the spread syntax ({ ...userDetails }). This syntax creates a shallow copy of the userDetails object, 		meaning that the top-level properties are copied, but nested objects are still referenced.</li>
	<li><b>case 1</b> : Although userDetails.age was changed to 22, cloneUserDetails still holds the original value of 20. This is because the spread syntax only creates a shallow 		copy, so the age property of cloneUserDetails remains unchanged.</li>
	<li><b>case 2</b> : The nested address object is still referenced by cloneUserDetails, so when the city property of userDetails.address is changed, it reflects in 				cloneUserDetails.address as well. Therefore, the output is "Banglore".</li>
	</ul>
	
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**
