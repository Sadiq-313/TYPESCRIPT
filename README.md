# TypeScript Learning Notes 🚀

A comprehensive collection of TypeScript concepts, practical examples, and exercises, starting from the fundamentals and progressing towards advanced topics.

# 1. Introduction to TypeScript

## What is TypeScript?

TypeScript is a strongly typed programming language built on top of JavaScript. It adds static type checking and helps developers catch errors during development.

## Why TypeScript?

- Type Safety
- Better Debugging
- Code Readability
- Better IDE Autocomplete
- Easier Maintenance
- Better Developer Experience

## JavaScript vs TypeScript

| JavaScript | TypeScript |
|---|---|
| Dynamically typed | Statically checked |
| `.js` extension | `.ts` extension |
| No built-in type annotations | Supports type annotations |
| Type errors may appear at runtime | Many type errors detected during development |

## Installation

```bash
npm init -y
npm install -D typescript
npx tsc --init
```

## First TypeScript Program

```typescript
let username: string = "Sadiq";

console.log(username);
```

## Compilation

```bash
npx tsc index.ts
node index.js
```

# 2. Basic Data Types

Data types define what kind of values a variable can store.

## String

Used to store text values.

```typescript
let username: string = "Sadiq";
let city: string = "Karachi";
```

## Number

Used to store numerical values, including integers and decimals.

```typescript
let age: number = 20;
let price: number = 1500.50;
```

## Boolean

Used to store true or false values.

```typescript
let isLoggedIn: boolean = true;
let isAdmin: boolean = false;
```

## Array

Used to store multiple values of the same type.

```typescript
let skills: string[] = [
    "JavaScript",
    "React",
    "Node.js"
];

let marks: number[] = [80, 90, 85];
```

## Object

Used to store related information in key-value pairs.

```typescript
let user: {
    name: string;
    age: number;
    isActive: boolean;
} = {
    name: "Sadiq",
    age: 20,
    isActive: true
};
```

### Optional Properties

Use `?` to define an optional property.

```typescript
let user: {
    name: string;
    email?: string;
} = {
    name: "Sadiq"
};
```

# 3. Type Inference

## What is Type Inference?

Type Inference is a feature in TypeScript that automatically determines the data type of a variable based on its assigned value.

We don't always need to explicitly define the type. TypeScript can understand the type automatically.

### Example

```typescript
let username = "Sadiq";

let age = 20;

let isLoggedIn = true;
```

TypeScript automatically understands:

- `username` → string
- `age` → number
- `isLoggedIn` → boolean

### Type Inference in Action

```typescript
let username = "Sadiq";

username = "Ali"; // Correct

username = 123; // Error
```

**Explanation:** TypeScript infers that `username` is a string. Therefore, assigning a number produces a type error.

### Key Points

- TypeScript automatically detects data types.
- It reduces unnecessary type annotations.
- It improves code readability.
- It helps prevent type-related errors.

# 4. Type Annotation

## What is Type Annotation?

Type Annotation is the process of explicitly specifying the data type of a variable, function parameter, or return value.

We use a colon (`:`) to specify a type.

### Syntax

```typescript
let variableName: dataType = value;
```

### Example

```typescript
let username: string = "Sadiq";

let age: number = 20;

let isLoggedIn: boolean = true;
```

### Function Type Annotation

We can also define types for function parameters and return values.

```typescript
function add(a: number, b: number): number {
    return a + b;
}

console.log(add(10, 20));
```

**Output:**

```text
30
```

Here:

- `a: number` defines the first parameter type.
- `b: number` defines the second parameter type.
- `: number` after the parentheses defines the return type.

### Incorrect Example

```typescript
function add(a: number, b: number): number {
    return a + b;
}

add("10", 20); // Error
```

**Explanation:** The function expects two numbers, but a string is provided as the first argument.

### Key Points

- Type Annotation explicitly defines data types.
- It improves code clarity.
- It helps detect incorrect values.
- It is useful for functions, variables, and objects.

# 5. Union Types

## What are Union Types?

Union Types allow a variable to store values of more than one specified data type.

We use the pipe (`|`) symbol to define a Union Type.

### Syntax

```typescript
let variableName: type1 | type2;
```

### Example

```typescript
let userId: string | number;

userId = 101;       // Correct

userId = "USER101"; // Correct

userId = true;      // Error
```

**Explanation:** The `userId` variable can accept either a string or a number, but not a boolean.

### Union Types with Functions

```typescript
function displayId(id: string | number): void {
    console.log("User ID:", id);
}

displayId(101);

displayId("USER101");
```

**Output:**

```text
User ID: 101
User ID: USER101
```

### Union Types with Type Narrowing

Sometimes we need to perform different operations depending on the actual type of a value.

We can use `typeof` to check the type.

```typescript
function printValue(value: string | number): void {

    if (typeof value === "string") {
        console.log(value.toUpperCase());
    } else {
        console.log(value.toFixed(2));
    }

}

printValue("typescript");

printValue(100);
```

**Output:**

```text
TYPESCRIPT
100.00
```

**Explanation:**

- If the value is a string, `toUpperCase()` converts it into uppercase.
- If the value is a number, `toFixed(2)` formats it to two decimal places.

This process is called **Type Narrowing**.

### Key Points

- Union Types allow multiple specified data types.
- The `|` symbol is used to define unions.
- They make variables and functions more flexible.
- Type Narrowing helps safely work with different types.

# 6. Difference Between Type Inference, Type Annotation and Union Types

| Concept | Meaning |
|---|---|
| Type Inference | TypeScript automatically detects the type. |
| Type Annotation | Developer explicitly defines the type. |
| Union Types | A value can have multiple specified types. |

### Quick Comparison

```typescript
// Type Inference
let name = "Sadiq";

// Type Annotation
let age: number = 20;

// Union Type
let id: string | number = 101;
```

# 7. Practical Exercises

Try solving these exercises without looking at the examples above.

1. Create a variable using Type Inference for your name.
2. Create a variable using Type Annotation for your age.
3. Create a variable that accepts both string and number.
4. Create a function that accepts two numbers and returns their sum.
5. Create a function that accepts string or number and uses `typeof` to identify its type.

# 8. Key Takeaways

- TypeScript is built on JavaScript.
- TypeScript helps detect type-related errors.
- TypeScript files use the `.ts` extension.
- TypeScript compiles into JavaScript.
- Basic types include string, number, boolean, array and object.
- Type Inference automatically detects data types.
- Type Annotation explicitly defines data types.
- Union Types allow multiple specified types.
- Type Narrowing helps TypeScript safely identify and work with specific types.

---

⭐ **Learning TypeScript one concept at a time!**

*This repository documents my continuous journey of learning TypeScript through practical examples and hands-on exercises.*
