# We've earned some iteration helpers

- Why would we want iteration helpers?

## Basic for loops

```javascript
const arr = [1, 2, 3, 4, 5];

for (let i = 0; i < arr.length; i++) {
  console.log(arr[i]);
}
```

## [For...of loops](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...of)

- The for...of loop allows you to iterate over arrays with a cleaner syntax.

```javascript
const arr = [1, 2, 3, 4, 5];

for (let value of arr) {
  console.log(value);
}
```

## [The Array forEach method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)

- You can call the forEach method on any array and pass it a callback function to execute on each item in the array.

```javascript
const arr = [1, 2, 3, 4, 5];

arr.forEach((element) => {
  console.log(element);
});
```

### Mini lab

1. Visit the array forEach MDN or w3 school and explain how we might access the _index_ of the current element.
2. What else can we optionally access?
3. Use a for loop, a for..of loop, and the forEach method to print out each number in arr multiplied by 100
4. Use a for loop, a for..of loop, and the forEach method to print out only numbers greater than 3
5. Use a for loop, a for..of loop, and the forEach method to add up all the numbers and print out the result

## Map, filter, and reduce

### With food first!

![map, filter, reduce with emoji](https://i.redd.it/yf7rw3pjiapx.jpg)

- Map, filter, and reduce are three array methods that make working with lists easier. These and other similar methods are often used in place of for looping in purely functional languages.

### [map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)

- "The map() method creates a new array with the results of calling a provided function on every element in this array."

```javascript
const arr = [1, 2, 3, 4, 5];

const newArr = arr.map((element) => {
  return element + 1;
});
```

### [filter](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)

- "The filter() method creates a new array with all elements that pass the test implemented by the provided function."

```javascript
const arr = [1, 2, 3, 4, 5];

const newArr = arr.filter((element) => {
  return element % 2 === 0;
});
```

### [reduce](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce)

- "The reduce() method applies a function against an accumulator and each element in the array (from left to right) to reduce it to a single value."

```javascript
const arr = [1, 2, 3, 4, 5];

const newArr = arr.reduce((accumulator, value) => {
  return accumulator + value;
}, 0);
```

__NOTE__ The single value returned can be an object or array. Often in examples it's a number or string but you can return anything. Reduce is extremely powerful and all other iterators can be written using it. It's tough to wrap one's mind around so don't worry if this one is inscrutable for now. We'll revisit it now and again...and again and again.

### Method chaining & using declared functions

- When using these array methods we can method chain. So instead of doing:

```javascript
const arr = [1, 2, 3, 4, 5];

const newArr = arr.map((element) => {
  return element + 1;
});

const newerArr = newArr.filter((element) => {
  return element % 2 === 0;
});
```

We can do:

```javascript
const arr = [1, 2, 3, 4, 5];

const newArr = arr.map((element) => {
  return element + 1;
}).filter(function(element) {
  return element % 2 === 0;
});
```

Furthermore, we don't have to inline the anonymous functions, we can declare them elsewhere:

```javascript
const arr = [1, 2, 3, 4, 5];

function add1(num) {
  return num + 1;
}

function isEven(num) {
  return num % 2 === 0;
}

const newArr = arr.map(add1).filter(isEven);
```

### Bonus Challenge

Write your own `map` and `filter` using only `reduce` (i.e. no for loops)
