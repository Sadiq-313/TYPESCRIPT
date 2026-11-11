# TypeScript Learning Notes

## Day 1 — Introduction to TypeScript

### What is TypeScript?
TypeScript is a strongly typed programming language built on top of JavaScript. It adds static type checking and helps developers catch errors during development.

### Why TypeScript?
- Type safety
- Better debugging
- Code readability
- Better IDE autocomplete
- Easier maintenance
- Better developer experience

### JavaScript vs TypeScript

| JavaScript | TypeScript |
|---|---|
| Dynamically typed | Statically checked |
| `.js` extension | `.ts` extension |
| No built-in type annotations | Supports type annotations |
| Type errors may appear at runtime | Many type errors detected during development |

### Installation

```bash
npm init -y
npm install -D typescript
npx tsc --init
```

### First TypeScript Program

```typescript
let username: string = "Sadiq";

console.log(username);
```

### Compilation

```bash
npx tsc index.ts
node index.js
```

---

## Day 2 — Basic Data Types

### 1. String

Used to store text values.

```typescript
let username: string = "Sadiq";
let city: string = "Karachi";
```

### 2. Number

Used to store numerical values, including integers and decimals.

```typescript
let age: number = 20;
let price: number = 1500.50;
```

### 3. Boolean

Used to store true or false values.

```typescript
let isLoggedIn: boolean = true;
let isAdmin: boolean = false;
```

### 4. Array

Used to store multiple values of the same type.

```typescript
let skills: string[] = [
    "JavaScript",
    "React",
    "Node.js"
];

let marks: number[] = [80, 90, 85];
```

### 5. Object

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

---

## Key Takeaways

1. TypeScript is built on JavaScript.
2. TypeScript helps detect type-related errors.
3. TypeScript files use the `.ts` extension.
4. TypeScript compiles into JavaScript.
5. Basic types include string, number, boolean, array and object.
6. Type annotations help define the expected data type.
