# Array methods and callback functions
_Callbacks functions and array methods can confuse some people when starting their journey as a developer. So let's reinforce our knowledge on Array methods and callbacks functions by breaking things down and going over some examples._

![]()
**`Callback functions`**


_First, we'll go over callback functions. A callback function is a function passed to another function as a parameter._


```javascript
const add = (a,b) => {
  return a + b
}

function multiply(a,b) {
  return a*b
}

const solutionLogger = (a,b, callback) => {
  const solution = callback(a, b)
  console.log('the solution is ' + solution)
}

solutionLogger(2,4, add) //the solution is 6
solutionLogger(2,5, multiply) //the solution is 10
```
_In the code above add() and multiply() would be our callback function. Both functions are provided to solutionLogger(). solutionLogger() then calls the callback function and logs out the solution._ </br>
### 1. `map()`
This method creates a new array with the results of calling a provided function on every element in this array.

**Example:**
```javascript
const numbers = [1, 2, 3];
const doubled = numbers.map(num => num * 2);
console.log(doubled); // [2, 4, 6]
```
### 2. `filter()`
This method creates a new array with only elements that pass the condition inside the provided function.

**Example:**
```javascript
const numbers = [1, 2, 3, 4];
const evenNumbers = numbers.filter(num => num % 2 === 0);
console.log(evenNumbers); // [2, 4]
```
### 3.`sort()`
This method is used to arrange/sort array’s elements either in ascending or descending order.

**Example:**
```javascript
const numbers = [4, 2, 3, 1];
const sortedNumbers = numbers.sort((a, b) => a - b);
console.log(sortedNumbers); // [1, 2, 3, 4]
```
### 4. `forEach()`
This method helps to loop over an array by executing a provided callback function for each element in an array.

**Example:**
```javascript
const numbers = [1, 2, 3];
numbers.forEach(num => console.log(num)); // 1, 2, 3
```
### 5. `concat()`
This method is used to merge two or more arrays and returns a new array, without changing the existing arrays.

**Example:**
```javascript
const arr1 = [1, 2];
const arr2 = [3, 4];
const merged = arr1.concat(arr2);
console.log(merged); // [1, 2, 3, 4]
```
### 6. `every()`
This method checks every element in the array that passes the condition, returning true or false as appropriate.

**Example:**
```javascript
const numbers = [2, 4, 6];
const allEven = numbers.every(num => num % 2 === 0);
console.log(allEven); // true
```
### 7. `some()`
This method checks if at least one element in the array passes the condition, returning true or false as appropriate.

**Example:**
```javascript
const numbers = [1, 2, 3];
const hasEven = numbers.some(num => num % 2 === 0);
console.log(hasEven); // true
```
### 8. `includes()`
This method checks if an array includes the element that passes the condition, returning true or false as appropriate.

**Example:**
```javascript
const numbers = [1, 2, 3];
const hasTwo = numbers.includes(2);
console.log(hasTwo); // true
```
### 9. `join()`
This method returns a new string by concatenating all of the array’s elements separated by the specified separator.

**Example:**
```javascript
const words = ['Hello', 'world'];
const sentence = words.join(' ');
console.log(sentence); // "Hello world"
```
### 10. `reduce()`
This method applies a function against an accumulator and each element in the array to reduce it to a single value.

**Exampple:**
```javascript
const numbers = [1, 2, 3];
const sum = numbers.reduce((acc, num) => acc + num, 0);
console.log(sum); // 6
```
### 11. `find()`
This method returns the value of the first element in an array that passes the test in a testing function.

**Example:**
```javascript
const numbers = [1, 2, 3, 4];
const firstEven = numbers.find(num => num % 2 === 0);
console.log(firstEven); // 2
```
### 12. `findIndex()`
This method returns the index of the first element in an array that passes the test in a testing function.

**Example:**
```javascript
const numbers = [1, 2, 3, 4];
const index = numbers.findIndex(num => num % 2 === 0);
console.log(index); // 1
```
### 13. `indexOf()`
This method returns the index of the first occurrence of the specified element in the array, or -1 if it is not found.

**Example:**
```javascript
const numbers = [1, 2, 3];
const index = numbers.indexOf(2);
console.log(index); // 1
```
### 14. `fill()`
This method fills the elements in an array with a static value and returns the modified array.

**Example:**
```javascript
const numbers = [1, 2, 3];
numbers.fill(0);
console.log(numbers); // [0, 0, 0]
```
### 15. `slice()`
This method returns a new array with specified start to end elements.

**Example:**
```javascript
const numbers = [1, 2, 3, 4];
const sliced = numbers.slice(1, 3);
console.log(sliced); // [2, 3]
```
### 16. `reverse()`
This method reverses an array in place. The element at the last index will be first and the element at the 0 index will be last.

**Example:**
```javascript
const numbers = [1, 2, 3];
numbers.reverse();
console.log(numbers); // [3, 2, 1]
```
### 17. `push()`
This method adds one or more elements to the end of the array and returns the new length of the array.

**Example:**
```javascript
const numbers = [1, 2];
const newLength = numbers.push(3);
console.log(newLength); // 3
console.log(numbers); // [1, 2, 3]
```


