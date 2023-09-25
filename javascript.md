## JavaScript interview questions and answers

#### Q: What is the ***object*** type?
A: The Object type represents one of JavaScript's data types. It is used to store various keyed collections and more complex entities. Objects can be created using the Object() constructor or the object initializer / literal syntax.
``` javascript
const obj = {
  foo: 1,
  // You should not define such a method on your own object,
  // but you may not be able to prevent it from happening if
  // you are receiving the object from external input
  propertyIsEnumerable() {
    return false;
  },
};

const normalObj = {}; // create a normal object
const nullProtoObj = Object.create(null); // create an object with "null" prototype
```
#### Q: Explain arrays in javascript.
A: An array is a special variable, which can hold more than one value and you can access the values by referring to an index number. 
- JavaScript arrays are resizable and can contain a mix of different data types.
- JavaScript arrays are not associative arrays and so, array elements cannot be accessed using arbitrary strings as indexes, but must be accessed using nonnegative integers (or their respective string form) as indexes.
- JavaScript arrays are zero-indexed: the first element of an array is at index 0, the second is at index 1, and so on — and the last element is at the value of the array's length property minus 1.
- JavaScript array-copy operations create shallow copies. (All standard built-in copy operations with any JavaScript objects create shallow copies, rather than deep copies).

Using an array literal is the easiest way to create a JavaScript Array.
``` javascript
const array_name = [item1, item2, ...];  
```
The following example also creates an Array, and assigns values to it:
``` javascript
const cars = new Array("Saab", "Volvo", "BMW");  
```

#### Q: What is the ***every()*** method of an array?
A: The every() method is an iterative method. It calls a provided callbackFn function once for each element in an array, until the callbackFn returns a falsy value. If such an element is found, every() immediately returns false and stops iterating through the array. Otherwise, if callbackFn returns a truthy value for all elements, every() returns true.

every acts like the "for all" quantifier in mathematics. In particular, for an empty array, it returns true. (It is vacuously true that all elements of the empty set satisfy any given condition.)

callbackFn is invoked only for array indexes which have assigned values. It is not invoked for empty slots in sparse arrays.
``` javascript
const isBelowThreshold = (currentValue) => currentValue < 40;

const array1 = [1, 30, 39, 29, 10, 13];

console.log(array1.every(isBelowThreshold));
// Expected output: true

function isBigEnough(element, index, array) {
  return element >= 10;
}
[12, 5, 8, 130, 44].every(isBigEnough); // false
[12, 54, 18, 130, 44].every(isBigEnough); // true

```

#### Q: What is the ***typeof*** operator?
A: The *typeof* operator returns a string indicating the type of the operand's value. You can use the typeof operator to find the data type of a JavaScript variable.

``` javascript
typeof "John"                 // Returns "string"
typeof 3.14                   // Returns "number"
typeof NaN                    // Returns "number"
typeof false                  // Returns "boolean"
typeof [1,2,3,4]              // Returns "object"
typeof {name:'John', age:34}  // Returns "object"
typeof new Date()             // Returns "object"
typeof function () {}         // Returns "function"
typeof myCar                  // Returns "undefined" *
typeof null                   // Returns "object"
```
Note: *You cannot use typeof to determine if a JavaScript object is an array (or a date).*
