
- In javascript, functions can live anywhere and data can be passed freely without being in any pre-defined classes.

### Types as Sets
- In TS, every type is just a set. Unlike java, where a variable can either be a string or an int at a time, in TS the variables can belong to many types/sets at a time. It is better to understand that types are just sets in TS
- How do you describe a value that either belongs in the `string` set or the `number` set? It simply belongs to the _union_ of those sets: `string | number`.

### Static Type Checking
- TS helps us with static type checking, we wouldn't have to wait till the runtime to know that our code is wrong

### Typescript Compiler
- TSC stands for typescript compiler. It is a type checker.
- The Typescript compiler converts the .ts file to a javascript
- Type annotations are not a part of ECMAScript, so we cannot directly run TS files, therefore we need a compiler which converts it JS so that it can be run

### Emitting with errors
- Even if we have type-errors in our code the TSC will change the .js file, because one of the core values of typescript is *most of the times, you know better than typescript*
- We can use *noEmitOnError* command if we do not want the TSC to change the js file in case of type-errors.

### DownLeveling
- TSC converts ts into js file, it can target any ECMAScript version it wants. By default it target the ECMA-5 version which is a bit old. 
- We can change it by using *tsc --target es2015 hello.ts* such commands

### Strictness
- If we are making a new project, we should always make sure to use *"strict": true*, so that we get most out of the typescript tooling.
- We should also use *noImplicitAny* and *strictNullChecks* flags to make sure we are getting the most out of the ts tooling

____________________________________________________

## Everyday Types

- TS has *any* type, whenever we do not want it any type-error for a variable 
- In most cases we do not have to define types for our variables, TS tries to infer the type whenever it can.

### Functions
- TS allows types for both input and output values in functions
- If a function returns a Promise, we have a Promise type as well which we can use.
- 


