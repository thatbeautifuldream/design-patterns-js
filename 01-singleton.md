# Singleton Design Pattern

- In singleton design pattern only one object is created for each interface (class or function) and the same object is returned whenever the function or class is called.

## Example

```javascript
const object1 = Singleton.getInstance();
const object2 = Singleton.getInstance();
console.log(object1 === object2); // true
```

## Implementation

- We can implement the singleton pattern by creating a closure with a variable that stores the created instance and returns it every time the function is called.

```javascript
const Singleton = function () {
  let instance;
  function createInstance() {
    const object = new Object("Instance of Singleton class");
    return object;
  }
  return {
    getInstance: function () {
      if (!instance) {
        instance = createInstance();
      }
      return instance;
    },
  };
};
```
