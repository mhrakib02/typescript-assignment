# Difference Between Type Alias and Interface in TypeScript

Introduction

TypeScript provides two important ways to define data structures: Type Aliases and Interfaces. Both are used to describe the shape of data and help developers write clean, readable, and organized code. Although they have similar purposes, they also have some differences.

 Detailed Body

A Type Alias uses the type keyword to create a new name for a type. It can define primitive types, object types, union types, and tuples.

Example:


type User = {
    name: string;
    age: number;
};

const user: User = {
    name: "Rakib",
    age: 22
};

Here I created a type called User with two properties: name and age. Now I can use User whenever I need an object with this structure.

An Interface uses the interface keyword to define the structure of an object. It is commonly used to describe object properties and class structures.

Example:

interface Student {
    name: string;
    age: number;
}
const student: Student = {
    name: "mehedi",
    age: 21
};

Here  the Student interface defines which properties an object should have.

One major difference is that interfaces support declaration merging. This means multiple interfaces with the same name can be combined. Type aliases do not support declaration merging. Interfaces can also extend other interfaces, while type aliases can combine types using intersections.

For

type Status = "active" | "inactive";


In practical development, interfaces are a good choice for defining object structures and working with classes. Type aliases are more useful when defining union types, tuples, primitive types, and complex type combinations. The choice depends on the project requirements.

Conclusion

Both Type Aliases and Interfaces are important features of TypeScript. They make code easier to understand and maintain. Understanding their differences helps developers choose the right option for different situations.
