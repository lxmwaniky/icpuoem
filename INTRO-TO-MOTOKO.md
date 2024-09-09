Motoko is a programming language that has been developed and optimized for creating programs built on the Internet Computer.

## Basic concepts and terms
- **Actor**: A unit of computation that can receive and send messages to other actors.
- **Canister**: A container for actors and their state.
- **Candid**: An interface description language for Motoko.
- **Principal**: A unique identifier for an actor or canister.
- **Service**: A collection of actors that can be accessed through a single interface.
- **Type**: A category of values that a variable can hold.
- **Declaration**: Used to define immutable variables, mutable state, objects, actors, classes, and other data types.
- **Expression**: Used to describe computations that involve declarations.
- **Program**: A collection of declarations and expressions that can be executed.

## Basic syntax
Motoko's program syntax uses declarations and expressions. Programs consist of an actor expression that is introduced using the keyword `actor`

```motoko
actor {
  // Actor body
}
```

### Snippets

```motoko
let x = 5; // Declaration
let y = 10 + x; // Declaration
x * y + x; // Expression
```

- Programme's type is `Nat` (natural number) because it is the result of a computation involving only natural numbers.

```motoko
let z = do {
  let x = 5;
  let y = 10 + x;
  x * y + x
};
```
- The variable z now stores the result value of 3, and can be called by additional methods.

### Using the base library
The base library includes a selection of modules that focus on the core features of Motoko.

To import the base library, the `import` keyword can be used at the start of your Motoko code file. After the `import` keyword, you need to provide a **local module name** and a **file path** that the import declaration can use to locate the imported module.

For example, to import a local module named 'Debug', you can use the following import statement:

```motoko
import Debug "mo:base/Debug";
```
Then, to use this imported library, you can call the module with a line of code such as:
```motoko
Debug.print("hello world");
```

Expressions can also be formed using a **block**. You can form a block expression from your list of declarations by enclosing it within curly brackets {}. A block expression is used to preserve the autonomy of the declaration list and the variable's names.

Blocks are only allowed as sub-expressions of **control flow expressions**. Control flow expressions are programming methods such as if, loop, case, etc. In any other place, you can use do { ... } to represent block expressions and distinguish blocks from object literals.

```motoko
do {
  let x = 1;
  let y = x + 1;
  x * y + x
}
```
Using the do { ... } expression allows our code to remain a functioning program, but now our declared variables x and y are privately scoped within the block expression you have defined.

Next, you can use a block expression to produce a value within a larger, compound expression, such as:
```motoko
100 +
  (do {
     let x = 1;
     let y = x + 1;
     x * y + x
   })
```
You can see that nesting blocks preserves the autonomy of each separate declaration list and its variable names. Language theorists refer to this as **lexical scoping**, where variables' scopes may nest, but do not interfere with one another as they nest.


## Defining an Actor

```motoko
actor {
  // Actor body
}
```
This actor definition is empty, meaning it does not define any data or send and receive messages.

```motoko
actor {
  let x = 40; let y = 2;
  ignore do {
    let x = 1;
    let y = x + 1;
    x * y + x
  };
  x + y
}
```

## Values and Evaluation
