# crazyJS

### Function Declaration
```
function add(a,b){
  return a + b
}
```

### Function Expression
```
var add = function(a,b){
  return a + b
}
```

### Arrow Expression
```
const add = function = (a,b) => {
  return a + b
}

```

| Feature  | Function Declaration | Function Expression | Arrow Function |
| ------------- | ------------- | ------ | ------- |
| Hoisting | Fully hoisted | Variable hoisted; function not | Not hoisted
| ``` this``` Binding  | Dynamic, based on invocation  | Dynamic, based on invocation |  invocation	Lexical, inherited from parent |
| Constructors | Can be used with ```new```  | Can be used with ```new``` | Cannot be used with ```new``` |

![Hoisting](https://res.cloudinary.com/dfh7pmyj0/image/upload/v1728057936/Screenshot_2024-10-04_213459_jzym65.png)

![TDZ](https://res.cloudinary.com/dfh7pmyj0/image/upload/v1728058055/Screenshot_2024-10-04_213716_f6uhot.png)


```
console.log(a);        // undefined (because 'var' is hoisted)
console.log(b);        // ReferenceError: Cannot access 'b' before initialization (TDZ)
console.log(c);        // ReferenceError: Cannot access 'c' before initialization (TDZ)
console.log(hello());  // "Hello, world!" (function declarations are fully hoisted)
console.log(funcExp);   // undefined (function expressions are hoisted as variables)
console.log(sum());    // ReferenceError: Cannot access 'sum' before initialization
console.log(arrow())  // ReferenceError: Cannot access 'arrFun' before initialization

var a = 10;
let b = 20;
const c = 30;

function hello() {
    return "Hello, world!";
}

var funcExp = function() {
    return "Function Expression";
};

let sum = function() {
    return "Sum Function";
};

const arrFun = () => {
  return "Arrow Function"
}

console.log(a);       // 10 (initialized now)
console.log(b);       // 20 (initialized now)
console.log(c);       // 30 (initialized now)
console.log(funcExp());  // "Function Expression"
console.log(sum());   // "Sum Function"
console.log(arrFun())  // "Arrow Function"
```
