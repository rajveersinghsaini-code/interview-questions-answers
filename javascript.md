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
