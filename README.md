# LearnTS
Here are some examples to help illustrate the concepts of static type system, interfaces, classes, and generics in TypeScript:

**Static Type System:**
TypeScript's type system is a static type system, meaning that the types are checked at compile time rather than runtime . This means that the TypeScript compiler can detect many common programming errors before the program is ever run .

For example:
```typescript
let myString: string = 'Hello';
myString = 5; // Error: Type 'number' is not assignable to type 'string'
```
In this example, we declare a variable `myString` with the type `string`. When we try to assign a number to `myString`, the TypeScript compiler gives us an error because a number is not assignable to a string.

**Interfaces:**
An interface in TypeScript is a way to define the shape of an object. It allows you to specify the properties and methods that an object must have.

For example:
```typescript
interface Person {
  name: string;
  age: number;
}

function greet(person: Person) {
  return `Hello ${person.name}, you are ${person.age} years old.`;
}

let john: Person = { name: 'John', age: 25 };
console.log(greet(john)); // Output: Hello John, you are 25 years old.
```
In this example, we define an interface `Person` with two properties: `name` and `age`. We then use this interface as the type for the parameter of the `greet` function. When we call the `greet` function with an object that has the shape defined by the `Person` interface, everything works as expected.

**Classes:**
A class in TypeScript is a blueprint for creating objects. It defines the properties and methods that an object will have.

For example:
```typescript
class Rectangle {
  width: number;
  height: number;

  constructor(width: number, height: number) {
    this.width = width;
    this.height = height;
  }

  getArea() {
    return this.width * this.height;
  }
}

let myRectangle = new Rectangle(5, 10);
console.log(myRectangle.getArea()); // Output: 50
```
In this example, we define a class `Rectangle` with two properties (`width` and `height`) and one method (`getArea`). We then create an instance of this class using the `new` keyword and call its `getArea` method to calculate the area of the rectangle.

**Generics:**
Generics in TypeScript allow you to write reusable code that can work with different types. They provide a way to create components that can work with any data type, not just one specific type.

For example:
```typescript
function identity<T>(arg: T): T {
  return arg;
}

let myString = identity<string>('Hello');
let myNumber = identity<number>(5);
```
In this example, we define a generic function `identity` that takes an argument of any type and returns a value of that same type. We then use this function with two different types (`string` and `number`) to demonstrate its reusability.
