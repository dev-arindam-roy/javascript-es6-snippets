# Javascript ES 5/6 Code Snippets

```
console.log(x); // output: undefined (x is not declared as variable)
console.log(typeof x); // output: "undefined" (type of x is "undefined" type)
console.log(typeof typeof x); // output: "string" ("undefined" is a string)
console.log(typeof x === 'undefined'); // output: true (type of x is "undefined" type and its string)
console.log(x === undefined); // output: true (value of x is undefined)

var x = 10;
```

```
var x = 10;
console.log(x); // Output: 10
console.log(typeof x); // Output: "number"
console.log(typeof typeof x); // Output: "string"
console.log(x == 10); // Output: true
console.log(x === 10); // Output: true
console.log(x == '10'); // Output: true
console.log(x === '10'); // Output: false (not exact match)
```

```
var x = '10';
console.log(x); // Output: "10"
console.log(typeof x); // Output: "string"
console.log(typeof typeof x); // Output: "string"
console.log(x == '10'); // Output: true
console.log(x === '10'); // Output: true
console.log(x == 10); // Output: true
console.log(x === 10); // Output: false (not exact match)
```

```
var x;
console.log(x); // Output: undefined
console.log(typeof x); // Output: "undefined"
console.log((x) ? true : false); // Output: false

x = null;
console.log(x); // Output: null
console.log(typeof x); // Output: "object"
console.log(typeof typeof x); // Output: "string"
console.log((x) ? true : false); // Output: false
```


```
// global scope
var x; 
let y;

if (true) {
  // block scope
}

function fun1() {
  // function scope
  if (true) {
    // block scope within function scope
  }
}
```


```
let x;
x = 100;
console.log(x); // Output: 100
x = 200;
console.log(x); // Output: 200
let x = 400;
console.log(x); // Output: error (SyntaxError: Identifier 'x' has already been declared)
```

```
let x; 
x = 100;

/** block scope */
if (true) {
  let x = 200;
  console.log(x); // 200
}

console.log(x); // 100
```


```
let x;

x = 100;
console.log(x); // 100

function fun1() {
    console.log(x); // 100
}

fun1();
console.log(x); // 100
```

```
let x;

x = 100;
console.log(x); // 100

function fun1() {
    let x = 200;
    console.log(x); // 200
}

fun1();
console.log(x); // 100
```

```
let x; /** global scope */ 

x = 100; 
console.log(x); // 100

/** funation scope */
function fun1() {
    let x = 200; /** function's global scope */
    if (true) {
      let x = 300; /** block scope */
      console.log(x); // 300
    }
    console.log(x); // 200
}

fun1();
console.log(x); // 100
```

