Javascript
==========

Table of Contents
-----------------

* [Basics](https://github.com/SyedAfrozPasha/Javascript/tree/develop#basics)
* [Advanced](https://github.com/SyedAfrozPasha/Javascript/tree/develop#advanced)

Basics
------

* JavaScript is a cross-platform, object-oriented scripting language used to make webpages interactive (e.x. having complex animations, clickable buttons, popup menus, etc.).  There are also more advanced server side versions of javascript such as Node.Js which allow you to add more functionality to a website than simply downloading files (such as realtime collaboration between multiple computers).

* JavaScript is case-sensitive and uses the Unicode character set.

* In JavaScript, instructions are called _statements_ (it is a line of code commanding a task. Every program consists of a sequence of statements.) and are separated by semicolons `;`.

* The source text of JavaScript script gets scanned from left to right and is converted into a sequence of input elements which are tokens, control characters, line terminators, comments, or whitespace. Spaces, tabs, and newline characters are considered whitespace.

* **_Comments:_**

  Comments behave like whitespace and are discarded during script execution.

  ```javascript

  // a one line comment

  /* this is a longer, 
  * multi-line comment
  */

  ```

* **_Identifier:_**

  A sequence of characters in the code that identifies a variable, function, or property.

* In JavaScript, _identifiers_ can contain only alphanumeric characters (or `$` or `_` ), and may not start with a digit.

* **_Declarations:_**

  There are three kinds of declarations in JavaScript.

  1. `var`

      Declares a variable, optionally initializing it to a value.

  2. `let`

      Declares a block-scoped, local variable, optionally initializing it to a value.

  3. `const`

      Declares a block-scoped, read-only named constant.

* A variable declared using the `var` or `let` statement with no assigned value specified has the value of undefined.

* A constant cannot change value through assignment or be re-declared while the script is running. It must be initialized to a value. However, the properties of `objects` or `array` assigned to constants are not protected (i.e. We can change the value inside the object or array).

* The `undefined` value behaves as `false` when used in a boolean context.

* The `undefined` value converts to `NaN` when used in numeric context.

  ```javascript

  var a; // a is undefined
  a + 2; // return NaN

  ```

* When you evaluate a `null` variable, the `null` value behaves as `0` in numeric contexts and as `false` in boolean contexts.

* When you declare a variable outside of any function, it is called a _global variable_, because it is available to any other code in the current document.

* When you declare a variable within a function, it is called a _local variable_, because it is available only within that function.

* _Hoisting_: Variables in JavaScript are in a sense "hoisted" or lifted to the top of the function or statement. Variables that are hoisted return a value of `undefined`.

* Because of _hoisting_, all `var` statements in a function should be placed as near to the top of the function as possible. This best practice increases the clarity of the code.

* In ECMAScript 2015 (ES6), `let` (`const`) does not hoist the variable to the top of the block. Referencing the variable in the block before the variable declaration results in a `ReferenceError`. The variable is in a "temporal dead zone" from the start of the block until the declaration is processed.

  ```javascript

  console.log(x); // ReferenceError
  let x = 3;

  ```

* For functions, only the function declaration gets hoisted to the top and not the function expression.

* _Global variables_ are in fact properties of the global object. In web pages, the global object is window, so you can set and access global variables using the `window.variable` syntax.

* JavaScript is a dynamically typed language. That means you don't have to specify the data type of a variable when you declare it, and data types are converted automatically as needed during script execution.

* A regex literal is a pattern enclosed between slashes.

* **_Conditional statements:_**

  A conditional statement is a set of commands that executes if a specified condition is true. JavaScript supports two conditional statements: `if...else` and `switch`.

* **_Falsy values:_**

  A falsy value is a value that translates to false when evaluated in a Boolean context.

  The following values evaluate to false (also known as Falsy values):

  * `false`
  * `undefined`
  * `null`
  * `0`
  * `NaN`
  * the empty string (`""`)

* Do not confuse the primitive boolean values true and false with the true and false values of the Boolean object. For example:

  ```javascript

  var b = new Boolean(false);
  if (b) // this condition evaluates to true
  if (b == true) // this condition evaluates to false

  ```

* **_Exception handling statements:_**

  You can throw exceptions using the `throw` statement and handle them using the `try...catch` statements.

* You can use a `catch` block to handle all exceptions that may be generated in the `try` block.

  ```javascript

  try {
    throw 'myException'; // generates an exception
  }
  catch (e) {
    // statements to handle any exceptions
    logMyErrors(e); // pass exception object to error handler
  }

  ```

* The `finally` block contains statements to execute after the try and catch blocks execute but before the statements following the `try...catch` statement. The `finally` block executes whether or not an exception is thrown. If an exception is thrown, the statements in the `finally` block execute even if no `catch` block handles the exception.

  ```javascript

  openMyFile();
  try {
    writeMyFile(theData); //This may throw an error
  } catch(e) {  
    handleError(e); // If we got an error we handle it
  } finally {
    closeMyFile(); // always close the resource
  }

  ```

* If the `finally` block returns a value, this value becomes the return value of the entire `try-catch-finally` production, regardless of any `return` statements in the `try` and `catch` blocks.

* Overwriting of `return` values by the `finally` block also applies to exceptions thrown or re-thrown inside of the `catch` block.

  [Read more on Exception handling statements](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#Exception_handling_statements)

* **_Promises:_**

  A Promise is in one of these states:

  * _pending_: initial state, not fulfilled or rejected.
  * _fulfilled_: successful operation
  * _rejected_: failed operation.
  * _settled_: the Promise is either fulfilled or rejected, but not pending.

  ![Promises](https://mdn.mozillademos.org/files/8633/promises.png "Promises")

  [Read more on Promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)

* The difference between a `for...of` loop and a `for...in` loop - While `for...in` iterates over **property names**, `for...of` iterates over **property values**.

* **_Function:_**

  Functions are one of the fundamental building blocks in JavaScript. A function is a JavaScript procedure — a set of statements that performs a task or calculates a value.

  Simple Function to calculate the factorial:

  ```javascript

  var factorial = function fac(n) {
    return n < 2 ? 1 : n * fac(n - 1);
  };

  console.log(factorial(3));

  ```

* **_Recursive function:_**

  A function that calls itself is called a _recursive function_.

* A function can refer to and call itself. There are three ways for a function to refer to itself:

  1. the function's name
  2. `arguments.callee`
  3. an in-scope variable that refers to the function

  For example, consider the following function definition:

  ```javascript

  var foo = function bar() {
    // statements go here
  };

  ```

  Within the function body, the following are all equivalent:

  1. `bar()`
  2. `arguments.callee()`
  3. `foo()`

Advanced
--------

* **_Syntax Parser_:**
  
  A program that reads your code and determines what it does and if its grammar or syntax is valid.

* **_Lexical Environment_:**

  Where something sits physically in the code you write.  

* **_Execution Context_:**

  The wrapper which help to manage the code that is running.
  There are lots of lexical environments. Which one is currently running is managed via execution contexts.

* **_Name/Value Pair_:**

  A name which maps to a unique value. The name may be defined more than once, but only can have one value in any given context. That value may be more name/value pairs.

* **_Object_:**

  A collection of name-value pairs.

  ```javascript
  // Example of an object
  let address = {
    street: 'Main',
    number: 100,
    apartment: {
      floor: 3,
      number: 301
    }
  }
  ```

* **_Execution context (Global)_:**
  * Execution context (Global) creates two things: _Global Object (`window` is case of browsers)_ and special variable called _`this`_.
  * Its been created by javascript engine.
  * Each window/tab has its own global execution context.
  * At global level, global object (`window`) is equal to `this`.
  * Execution context is created in two phases: **_Creation Phase_** and **_Execution Phase_**
  * In _Creation Phase_, Global Object, `this`, Outer environment and Hoisting are created.
  * In _Creation Phase_, Parser runs through the code and begins to setup translations such as where we have created variables or functions and setup memory space for variables and functions. This is called '**_Hoisting_**'.
* All variables in javascript are initially set to _undefined_ by javascript engine.
* _undefined_ is a special keyword or value in javascript. Its also one of a data type in javascript. It is assigned to a variable _which is declared but not defined_ by javascript engine.
* Defining a variable with _undefined_ is a bad practice and should be avoided.

  Example:

  ```javascript

    var a;
    console.log(a);
    if (a === undefined) { // undefined is a keyword
      console.log('a is undefined!');
    } else {
      console.log('a is defined!');
    }

  ```

* In Execution Phase, code is executed line by line.

* **_Single Threaded:_**

  It means one command is executed at a time.

* **_Synchronous:_**

  One line of code is executed at a time in order.

* Javascript is a _Single Threaded_ and _Synchronous_ execution in behavior.

* **_Invocation:_**

  Running or calling a function. In Javascript, a function is invoked using parenthesis `()`.

  Example:

  ```javascript
  function b() {
  }
  
  function a() {
    b();
  }

  a();
  ```

  Steps involved in execution:
  
  1. Firstly Global Execution Context is created.
  2. In Creation Phase, Global Object('window'), 'this' and setup memory space for function.
  3. In Execution Phase, Code is executed line by line.
  4. When it reached the line `a()`, a new execution context is created and placed on the top of _Execution Stack_. Then it run that code.
  5. Now when it reaches the line `b()`, a new execution context is created and placed on top on the `a()` execution context. Then it run that code.
  6. Then `b()` is executed and popped-off the execution stack.
  7. Similarly, `a()` is executed and popped-off the execution stack.

* Every function creates a new execution context and placed on top of the execution stack. When function is finishes execution, its popped-off the execution stack.

* **_Variable Environment:_**

  Where the variables live and how they relate to each other in memory. Each variable live in its own execution context.

  Example:

  ```javascript

  // Each variable live in its own execution context.

  function b() {
    var myVar;
    console.log(myVar); // output: undefined
  }

  function a() {
    var myVar = 2;
    console.log(myVar); // output: 2
    b();
  }

  var myVar = 1;
  console.log(myVar); // output: 1
  a();
  console.log(myVar); // output: 1
  ```

* Every execution context has a reference to its outer environment.

* Scope chain: lexical environment top to bottom. Outer reference that any running function has.

  Example:

  ```javascript
  // Example 1:
  // Here `b()` and `a()` are lexically sitting in the global environment.
  function b() {
    console.log(myvar); // output: 1
    // Every execution context has a reference to its outer environment.
    // Here outer lexical environment refers to Global execution context.
  }

  function a() {
    var myVar = 2;
    b();
  }

  var myVar = 1;
  a();

  ```

  ```javascript
  // Example 2:
  // Here `b()` is lexically sitting in the `a()` lexical environment.
  // and `a()` is lexically sitting in the global lexical environment.
  function a() {

    function b() {
      console.log(myvar); // output: 2
      // Here outer lexical environment refers to a() execution context.
    }

    var myVar = 2;
    b();
  }

  var myVar = 1;
  a();  
  ```

* **_Scope:_**

  Where a variable is available in the code.

* In ES6, `let` is used to declare the variable. It allows the javascript engine to use block scoping, Which means scope of a given variable is only bound to a given block of code. In execution phase, variable is placed in memory however we are not allowed to use it outside its block.

* **_Asynchronous:_**

  More than one at a time. Multiple piece of code executing at the same time.

* In browser, The javascript engine talks with the Rendering Engine which is outside the javascript engine. Rendering engine prints or renders the contents on the screen. This communication between the Rendering engine and Javascript engine is _asynchronous_ in nature. Whereas whats happening inside the javascript engine is _synchronous_ execution.

* Javascript Engine has list/queue to manage the events called _Event Queue_. Every event is placed on this queue when its called.

* Javascript Engine looks for _Event Queue_ after every execution context is popped-off the execution stack. Then when the execution stack is empty, events are processed from the _Event Queue_. For each event a new execution context is created on the execution stack.

* Browser places every event in _Event Queue_ asynchronously. Whereas Javascript engine execute it one by one synchronously.

* Long running functions interrupts the event calls. As the execution stack is not empty, the event are not processed.

* **_Dynamic Typing:_**

  We don't specify the javascript engine what type of data a variable should hold, instead its been figured out while the code is running/executing. Variables can hold different types of values because it's all figured out during execution.

* Javascript is _Dynamically Typed_. It means that there is no keyword in javascript to tell which type of variable is it.

* Javascript determines the variable type at the time of execution.

* **_Primitive Types:_**

  A type of data that represents a _single value_.

  There are 6 Primitive types in javascript:

  1. **undefined**: It represents lack of existence. It shouldn't be set/assigned to a variable.

  2. **null**: It also represents lack of existence. It can be set/assigned to a variable. Because JavaScript is case-sensitive, null is not the same as Null, NULL, or any other variant.

  3. **Boolean**: It represents the values such as `true` or `false`.

  4. **Number**: In javascript, it always represent to a floating point numbers(numbers with decimals)

  5. **String**: It is a sequence of characters enclosed in single or double quotes.

  6. **Symbol**: Its used in ES6 and next version. Its not fully supported by older browsers. It is a data type whose instances are unique and immutable.

* **_Operators:_**

  A special function that is syntactically (written) differently. Generally, operators take two parameters and return one result.

* Operators uses _infix notation_. Eg: 3 `+` 4

* _Infix notation_ is the notation commonly used in arithmetical and logical formulae and statements. It is characterized by the placement of operators between operands - "infixed operators" - such as the plus sign in 2 `+` 2.

* **_Operator Precedence:_**

  Which operator function gets called first. Functions are called in order of precedence.
  If more than one operators are present, the operator with higher precedence is called first.

* **_Associativity:_**

  In what order operator functions get called in: _left-to-right_ or _right-to-left_, when two or more operator  functions have the same precedence. _Left-to-Right_ is called _Left Associativity_ and _Right-to-Left_ is called _Right Associativity_.

  [Read more on operator precedence and associativity](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence)

  Example:

  ```javascript
  var a = 2, b = 3, c = 4;

  a = b = c;
  // Assignment operator has right-to-left associativity

  console.log(a); // output: 4
  console.log(b); // output: 4
  console.log(c); // output: 4
  ```

* **_Coercion:_**

  Converting a value from one type to another.

  Example:

  ```javascript

  // Coercion
  var a = 1 + '2';
  console.log(a); // output: 12

  console.log(3 < 2 < 1); // output: true

  Number(undefined); // NaN
  Number(null); // 0

  Boolean(undefined); // false
  Boolean(null); // false
  Boolean(""); // false
  Boolean(0); // false

  ```

* Its good practice to use `===` instead of `==` for equality check. In case of `==`, coercion occurs if it is comparing different data type. Whereas in `===`, coercion doesn't occur.

* `===` will return true on comparison only if the RHS of operator has same value and data type as the LHS of the operator.

  [Read more on Equality comparisons and sameness](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Equality_comparisons_and_sameness)

* Default Value:

  Example:

  ```javascript
  // In ES5
  function greet(name) {
    name = name || 'default value';
    console.log('Hello ' + name); // Hello default value
  }

  greet();

  ```

* Framework or Library is grouping of javascript code that performs a task and is intended to be reuseable.

* Object can have properties and methods. i.e, A object can have a _Primitive_ property, _Object_ property and _Function_ method. Object is sitting in memory and will have references to the addresses/spaces in memory of its properties and method.

* Object is said to have
  * _property_ - if its value is _Primitive_
  * _method_ - if its value is _Function_.

* Functions inside an object is called as _method_.

* _Computed member access operator_ is used to created new properties or methods for the object.

* _dot operator_ or _member access operator_ is also used to created new properties or methods for the object.

  ```javascript

  var person = new Object();
  person["firstName"] = "Syed"; // Computed member access operator

  person.lastName = "Pasha"; // dot operator/member access operator

  ```

* JavaScript is case-sensitive and uses the Unicode character set.

* An _object literal_ is a list of zero or more pairs of property names and associated values of an object, enclosed in curly braces (`{}`).

* **_Namespace:_**

  A container for variables and functions. Typically to keep variables and functions with the same name separate.

  Example:

  ```javascript

  var greet = 'Hello!';
  var greet = 'Hola!';

  console.log(greet); // output: Hola!
  // Collision or overriding of variables occurs here

  var english = {}; // Object literal syntax
  var spanish = {};

  english.greet = "Hello!";
  spanish.greet = "Hola!";
  // here greet value doesn't collide or override by the same variable name
  // here 'english' and 'spanish' act as container for the greet variable

  console.log(english);

  ```

* **JSON (JavaScript Object Notation)** is inspired by the object literal syntax. Here the property values must be enclosed in quotes. Technically, JSON is a subset of object literal syntax.

* In Javascript, `JSON.stringify()` is used to convert object to JSON and `JSON.parse()` is used to convert JSON to object.

  ```json

  // Example of JSON
  {
    "firstName": "Syed",
    "isAProgrammer": true
  }

  ```

  ```javascript

  var objectLiteral = {
    firstName: 'Syed',
    isAProgrammer: true
  }

  console.log(JSON.stringify(objectLiteral))
  // JSON.stringify() convert object into JSON

  ```

* **_First Class Functions:_**

  Everything you can do with other types you can do with functions. We can assign them to variables, pass them around as parameters to other functions, create them on the fly. Functions are special type of object in javascript. We can attach properties and methods to a function such as Primitive, Object and Function.

* In Javascript, Functions are object.
  
* In Javascript, Function object has some hidden special properties such as
  * _Name:_ Optional property - A function can have name or it can be anonymous (function without name).
  * _Code:_ its the actual line of code which we have written sit. It can be invocable (run this piece of code).

  Example:

  ```javascript
  
  // Functions are object
  function greet() {
    console.log('Hi');
  }
  // This function has properties:
  // Name: 'greet'
  // Code: console.log('Hi');

  greet.language = 'english';

  console.log(greet); // output: function greet() { console.log('Hi');}
  console.log(greet.language); // output: english

  ```

* **_Expression:_**

  A unit of code that results in a value. An expression return a value.

* **_Statement:_**

  A unit of code that doesn't results in a value. Statement doesn't return a value.

* Function Expression aren't hoisted. Only variable and function declaration are hoisted.

  ```javascript

  // Function Statement
  function greet() {
    console.log('Hi');
  }

  greet();


  // Function Expression
  var anonymousGreet = function() {
    console.log('Hi');
  }

  anonymousGreet();

  // -----------------------
  function log(a) {
    a();
  }

  // Passing a function as parameter - First Class Function
  // Function Expression
  log(function() {
    console.log('Hi');
  });

  ```

* **_By Value:_**

  All primitive types interact _by value_.

  ```javascript

  var a = 3; // 'a' has some primitive value & is stored in a memory location.

  var b = a; // Here value of 'a' is been copied to 'b', which is stored in some other location (other then 'a' location).

  a = 2; // change in value of 'a' does not affect the 'b'

  console.log(a); // output: 2
  console.log(b); // output: 3

  ```

* **_By Reference:_**

  All objects including functions interact _by reference_.

  ```javascript

  var a = {
    greeting: 'Hi'
  };
  // here 'a' is an object & is stored in a memory location.
  var b = a; // Here 'b' points to the same memory location of 'a'. No new object is created.

  a.greeting = 'Hello' // mutate

  console.log(a); // output: { greeting: 'Hello'};
  console.log(b); // output: { greeting: 'Hello'};

  // --------------------------------
  // by reference (even as parameters)

  function changeGreeting(obj) {
    obj.greeting = 'Hola'; // mutate
  }

  changeGreeting(b);

  console.log(a); // output: { greeting: 'Hola'};
  console.log(b); // output: { greeting: 'Hola'};

  // --------------------------------

  // Equals operator sets up new memory space (new address)
  // This is a special case where by references doesn't apply

  a = { greeting: 'Howdy' }; // Here new memory location was setup for 'a'
  // 'a' pointing to different spot in memory in this case

  console.log(a); // output: { greeting: 'Howdy'};
  console.log(b); // output: { greeting: 'Hola'};

  ```

* **_Mutate:_**

  To change something.

* **_Immutable:_**

  It means it can't be changed.

* **_this:_**

  ```javascript

  function a() {
    console.log(this); // Here 'this' points to global window object
    this.newVariable = 'hello'; // variables can be defined in global window object
  }

  var b = function() {
    console.log(this); // Here 'this' points to global window object
  }

  a();

  console.log(newVariable); // assigned variable can be used without this operator

  b();

  var c = {
    name: 'value',
    log: function() {
      this.name = 'Updated value'; // this will mutate the 'name' value

      console.log(this); // output: {name: 'Updated value',log: function() {console.log(this);}}
      // Here 'this' points to the 'c' object
      // It points to the object contains 'this'


      var setName = function(newName) {
        this.name = newName; // this will not mutate the 'name' property of 'c' object, instead this will mutate the 'name' variable in global window object.
      }
      setName('Updated Again!');
      console.log(this); // output: 'Updated value'
    }
  }

  c.log();

  ```

  ```javascript

  // The quirk can be avoided like this
  var c = {
    name: 'value',
    log: function() {
      var self = this; // assigning the reference of 'this' to a variable

      self.name = 'Updated value'; // this will mutate the 'name' value

      console.log(self); // Here 'this' points to the 'c' object


      var setName = function(newName) {
        self.name = newName; // this will mutate the 'name' property of 'c' object, not the global window object.
      }
      setName('Updated Again!');
      console.log(self); // output: 'Updated Again!'
    }
  }

  c.log();

  ```

* **_Arrays:_**

  Its a collection of same or different type of data.

  ```javascript

  // This is a valid array in javascript
  var arr = [
    1,
    false,
    {
      name: 'Syed'
    },
    function(name) {
      var greeting = 'Hello ';
      console.log(greeting + name);
    },
    "hello"
  ];

  arr[3](arr[2].name); // output: 'Hello Syed'

  ```

* A new execution context is created for any _function_, which will have 'Variable Environment', 'this', 'Outer Environment' and 'arguments'.

* **_Arguments:_**

  The parameters that are passed to a function. _arguments_ is a keyword which contains all the value or the parameters passed to a functions.

  ```javascript

  function greet(firstname, lastname, language) {

    if (arguments.length === 0) {
      console.log('Missing Parameters!');
      return;
    }
  
    console.log(firstname);
    console.log(lastname);
    console.log(language);
    console.log(arguments);
    console.log(arguments[0])
    console.log('---------');
  }

  greet();
  greet('Syed');
  greet('Syed', 'Pasha');
  greet('Syed', 'Pasha', 'English');

  ```

* **_Function Overloading:_**

  Function with a same name has different number of parameters. It doesn't work in javascript as functions are object.

  ```javascript

  function greet(firstname, lastname, language) {
    language = language || 'en';

    if (language === 'en') {
      console.log('Hello ' + firstname + ' ' + lastname);
    }

    if (language === 'es') {
      console.log('Hola ' + firstname + ' ' + lastname);
    }
  }

  function greetEnglish(firstname, lastname) {
    greet(firstname, lastname, 'en');
  }

  function greetSpanish(firstname, lastname) {
    greet(firstname, lastname, 'es');
  }

  greetEnglish('Syed', 'Pasha');
  greetSpanish('Syed', 'Pasha');

  ```

* Syntax Parsers reads the code character by character using a set of rules (valid syntax). It happens before the code is executed.

* Its recommended to put semicolon at the end of a line of code. If there is no semicolon is present, the syntax parser will automatically insert semicolon, which can lead to unexpected behavior.

  ```javascript

  function getPerson() {
    return // Here Syntax parser will automatically insert semicolon
    {
      firstname: 'Syed'
    }
  }

  console.log(getPerson()); // output: undefined

  ```

* Whitespace: Invisible characters that create literal 'space' in the written code.

* **_Immediately Invoked Function Expressions (IIFE)s:_**

  Immediately invoking a function expression.

  ```javascript

  // Example 1:
  var greeting = function(name) {
    console.log('Hello ' + name);
  }('Syed');

  console.log(greeting); // output: 'Hello Syed'


  // Example 2:
  // Function statements can be used without function name
  // () will trick the syntax parser to treat it as function expression
  (function (name) {
    var greeting = 'Hello';
    console.log(greeting + ' ' + name);
  }('Syed'));
  
  ```

* Below code execution of (IIFE) under the hood:
  * Firstly global execution context is created and the function object is placed in global execution context.
  * The when the functions is invoked, a new execution context is created. The variables defined inside the function will sit in the execution context of its function and not in global execution context.

  ```javascript

  (function (name) {
    var greeting = 'Hello';
    console.log(greeting + ' ' + name);
  }('Syed'));

  ```

  ```javascript

  // We can modify the global variable inside an IIFE, if we pass the global window object as parameter to the IIFE
  var greeting = 'Hola';
  (function (global, name) {
    var greeting = 'Hello';
    global.greeting = 'Hello';
    console.log(greeting + ' ' + name); // output: Hello Syed
  }(window, 'Syed'));
  console.log(greeting); // output: Hello

  ```

* **_Closures:_**

  ```javascript

  function greet(whattosay) {
    return function(name) {
      console.log(whattosay + ' ' + name);
    }
  }

  greet('Hi')('Syed');

  // or

  var sayHi = greet('Hi');
  sayHi('Syed');

  ```

  Steps:
  1. When this line `var sayHi = greet('Hi');` is executed, a new execution context is created for the `greet` function. And a new variable `whattosay` is setup in the variable environment. And the function in returned to variable `sayHi`. The `greet` function execution context is popped-off the execution stack.
  2. Then this line `sayHi('Syed')` is executed. Then a new execution context is created for `sayHi` function. `whattosay` variable is looked up in the scope chain where that variable is created (outer lexical environment reference).
  
  Function (execution context) which has reference to variables in its outer lexical environment. Execution context is closed in its outer variables to which it has reference even after the execution context is popped-off the execution stack. This phenomenon of closing in all the variables(free variables) that it suppose to have access to is called **_Closure_**. This is the feature of javascript language.

  ```javascript
  
  // Example of closure
  function buildFunctions() {
    var arr = [];

    for (var i = 0; i < 3; i++) {
        arr.push(function() {
            console.log(i);
          }
        )

        // arr.push((function(j) {
        //     return function() {
        //       console.log(j);
        //     }
        //   }(i))
        // )
    }

    return arr;
  }

  var fs = buildFunctions();

  fs[0](); // output: 3
  fs[1](); // output: 3
  fs[2](); // output: 3

  ```

* Function Factories: A function which return or make other things.

  ```javascript

  function makeGreeting(language) {
    return function (firstName, lastName) {
      if (language === 'en') {
        console.log('Hello ' + firstname + ' ' + lastname);
      }

      if (language === 'es') {
        console.log('Hola ' + firstname + ' ' + lastname);
      }
    }
  }

  var greetEnglish = makeGreeting('en');
  var greetSpanish = makeGreeting('es');

  greetEnglish('Syed', 'Pasha');
  greetSpanish('Syed', 'Pasha');

  ```

* **_Callback Function:_**

  A function which is given to another function, to be run when the other function is finished. So the function you call (invoke), 'calls back' by the calling the function you gave it when it finishes.

  ```javascript
  
  // Example of first-class function and closure
  function sayHiLater() {
    var greeting = 'Hi!';

    setTimeout(function() {
      console.log(greeting);
    }, 3000);
  }

  sayHiLater();

  ```

* All functions in javascript has access to the special methods such as `call`, `apply` and `bind`.

* **_Bind:_**

    Bind method return a new copy of the function. Reference of `this` object is passed as parameter to the bind method. It does not execute the function.

  ```javascript

  var person = {
    firstName: 'Syed',
    lastName: 'Pasha',
    getFullName: function() {
      var fullName = this.firstName + ' ' + this.lastName;
      return fullName;
    }
  }

  var logName = function(lang1, lang2) {
    console.log('Logged: ' + this.getFullName());
    console.log('Arguments: ', lang1, lang2);
  }

  logName(); // This will throw an error, as undefined is not a function

  var logPersonName = logName.bind(person); // Here this will point to person object

  logPersonName('en');

  ```

* **_Call:_**

  Call method works similar to the function call, except it let us control the `this` reference of that function. Call method actually executes the function.

  ```javascript

  var person = {
    firstName: 'Syed',
    lastName: 'Pasha',
    getFullName: function() {
      var fullName = this.firstName + ' ' + this.lastName;
      return fullName;
    }
  }

  var logName = function(lang1, lang2) {
    console.log('Logged: ' + this.getFullName());
    console.log('Arguments: ', lang1, lang2);
  }

  logName.call(person); // Here function is executed with 'this' reference of 'person' object

  logName.call(person, 'en', 'es'); // argument can also be passed

  ```

* **_Apply:_**

  Its very similar to `call` method, except the arguments are passed inside an array.

  ```javascript

  var person = {
    firstName: 'Syed',
    lastName: 'Pasha',
    getFullName: function() {
      var fullName = this.firstName + ' ' + this.lastName;
      return fullName;
    }
  }

  var logName = function(lang1, lang2) {
    console.log('Logged: ' + this.getFullName());
    console.log('Arguments: ', lang1, lang2);
  }

  logName.apply(person, ['en', 'es']); // argument has to be passed inside an array

  // Example 2:
  // Function borrowing: borrowing methods from other objects

  var person2 = {
    firstName: 'Afroz',
    lastName: 'Pasha'
  }

  person.getFullName.apply(person2);

  ```

* **_Function Currying:_**

  Creating a copy of a function but with some preset/default parameters. Its very useful in mathematical situation.

  ```javascript

  // Function Currying
  function multiply(a, b) {
    return a * b;
  }

  var multipleByTwo = multiply.bind(this, 2); // Here the first parameter is always set to 2

  multipleByTwo(4); // Here 4 will act as second parameter

  ```

* **_Functional Programming:_**

  Using first-class functions to segment the code.

  ```javascript
  
  // Example of Function programming

  // Example 1
  function mapForEach(arr, fn) {
    var newArr = [];
    for (var i = 0; i < arr.length; i++) {
      newArr.push(
        fn(arr[i])
      )
    }

    return newArr;
  }

  var arr1 = [1, 2, 3];
  console.log(arr1);

  var arr2 = mapForEach(arr1, function(item) {
    return item * 2;
  });

  console.log(arr2);


  // Example 2
  var checkPastLimit = function(limiter, item) {
    return item > limiter;
  }

  var arr3 = mapForEach(arr1, checkPastLimit.bind(this, 1));

  console.log(arr3);

  // Example 3
  var checkPastLimitSimplified = function(limiter) {
    return function(limiter, item) {
      return item > limiter;
    }.bind(this, limiter)
  }

  var arr4 = mapForEach(arr1, checkPastLimitSimplified(2));

  console.log(arr4);

  // Example 4
  // Using underscore.js library

  var arr5 = _.map(arr1, function (item) {
    return item * 3;
  })

  console.log(arr5);

  var arr6 = _.filter([2,3,4,5,6,7], function(item) {
    return item % 2 === 0;
  });

  console.log(arr6);

  ```

* **_Inheritance:_**

  One object gets access to the properties and methods of another object. Javascript uses prototypal inheritance.

* **_Prototype:_**

  * Each object has its own prototype called _proto_, which is also a object.
  * Object can share the prototype of other object.
  * If any property is not found in the given object, then it will look up the _prototype chain_ for that property in proto object.

  ```javascript

  var person = {
    firstName: 'Default',
    lastName: 'Default',
    getFullName: function() {
      var fullName = this.firstName + ' ' + this.lastName;
      return fullName;
    }
  }

  var syed = {
    firstName: 'Syed',
    lastName: 'Pasha'
  }

  // don't do this EVER! for demo purposes only!
  syed.__proto__ = person;
  console.log(syed.getFullName()); // output: Syed Pasha
  console.log(syed.firstName); // output: Syed

  var afroz = {
    firstName: 'Afroz'
  }

  afroz.__proto__ = person;
  console.log(afroz.getFullName()); // output: Afroz Default
  console.log(afroz.firstName); // output: Afroz

  ```

* A prototype of a prototype is an object.

* A base object is a bottom of prototype chain.

* A base object doesn't have a prototype.

  ```javascript

  var a = {};
  var b = function() {};
  var c = [];

  a.__proto__ ; // This will return a 'base object' - {}
  // This will have properties and methods of object


  b.__proto__ ; // This will return an 'empty function object' - function Empty() {}
  // This will be the prototype of all the function in javascript
  // This will have properties and methods of function


  c.__proto__ ; // This will return an empty array
  // This will have properties and methods of array

  ```

* **_Reflection:_**

  An object can look at itself, listing and changing its properties and methods.

  ```javascript

  var person = {
    firstName: 'Default',
    lastName: 'Default',
    getFullName: function() {
      var fullName = this.firstName + ' ' + this.lastName;
      return fullName;
    }
  }

  var syed = {
    firstName: 'Syed',
    lastName: 'Pasha'
  }

  // don't do this EVER! for demo purposes only!
  syed.__proto__ = person;

  // Reflection
  for (var prop in syed) {
    console.log(prop + ': ' + syed[prop]);
  }

  for (var prop in syed) {
    if (syed.hasOwnProperty(prop)) {
      console.log(prop + ': ' + syed[prop]);
    }
  }

  // Extend
  // Using underscore.js

  var b = {
    address: '111 Main St.'
    getFormalFullName: function() {
      return this.lastName + ', ' + this.firstName
    }
  }


  var c = {
    getFirstName: function() {
      return firstName;
    }
  }

  _.extend(syed, b, c);

  console.log(syed);

  ```

* **_Function constructor:_**

  A normal function that is used to construct objects. The `this` variable points a new empty object, and that object is returned from the function automatically.

  ```javascript

  function Person() {
    this.firstName = 'Syed';
    this.lastName = 'Pasha';
  }

  // Another way of creating object in javascript
  var syed = new Person(); // Here 'new' is an operator
  // Here 'new' operator will create empty object and then add/call the Person function, with the 'this' variable point to empty object
  console.log(syed);

  // ---------------------------

  function Person(firstName,lastName) {
    console.log(this);
    this.firstName = firstName;
    this.lastName = lastName;
  }

  var syed = new Person('Syed', 'Pasha');

  console.log(syed);

  var afroz = new Person('Afroz', 'Pasha');

  console.log(afroz);

  ```

* All Functions in javascript has some properties such as:
  * Name
  * Code
  * prototype: Its used only by the `new` operator. its not the prototype of the function. Its a prototype of any object created using function contructor.

* Any object created with function constructor, can be added with new features using _prototype_ property of function constructor.

* Methods created using prototype can be resued in all the object without creating a new memory space for that function/method.

  ```javascript

  function Person(firstName,lastName) {
    console.log(this);
    this.firstName = firstName;
    this.lastName = lastName;
    console.log('This function is invoked.');
  }

  Person.prototype.getFullName = function () {
    return this.firstName + ' ' + this.lastName;
  }

  var syed = new Person('Syed', 'Pasha');

  console.log(syed);

  var afroz = new Person('Afroz', 'Pasha');

  console.log(afroz);

  Person.prototype.getFormalFullName = function () {
    return this.lastName + ', ' + this.firstName;
  }

  console.log(syed.getFormalFullName());

  ```

* For prototype to work, we should define a function using `new` keyword. And the name of that function (function constructor) should be starting with Capital letter.

* Built-in function constructor:

  ```javascript

  // Here a will have property of number
  // This will create object
  var a = new Number('3');
  console.log(a); // Number {3}
  
  // Here b will have property of string
  var b = new String('Syed');
  console.log(b); // String {"Syed"}

  // We can add new feature using prototype
  String.prototype.isLengthGreaterThan = function(limit) {
    return this.length > limit;
  }

  console.log("Syed".isLengthGreaterThan(3));

  // --------------------------------

  var a = 3; // This one is primitive value
  var b = new Number(3); // This one will have object created with function constructor
  // This type of defining a variable should be avoided

  a == b // true

  a === b // false

  ```

* Its better not to used built-in function constructors, instead use actual primitive values.

* For iteration an array, don't use `for...in` instead use `for(var i = 0....)`.

  ```javascript

  Array.propotype.myCustomFeature = 'cool';

  var arr = ['a', 'b', 'c'];

  for (var prop in arr) {
    console.log(prop + ': ' + arr[prop]);
  }

  ```

* Pure prototypal inheritance:

  * `Object.create()` creates an empty object with its prototype pointing to what ever that is passed into the `Object.create()`.

  ```javascript

  var person = {
    firstName: 'Default',
    lastName: 'Default',
    greet: function() {
      return 'Hi ' + this.firstName;
    }
  }

  var syed = Object.create(person);
  console.log(syed); // returns Empty object, but prototype will have properties and methods of person object.

  syed.firstName = 'Syed';
  syed.lastName = 'Pasha';

  console.log(syed);

  ```

* **_Polyfill:_**

  code that adds a feature which the engine may lack.

* ES6 and Classes:

  ```javascript

  // Another way of creating an object

  // Here 'extends' keyword sets the prototype
  class InformalPerson extends Person {
    constructor (firstName, lastName) {
      super(firstName, lastName); // This will call the constructor of object which is the prototype
    }

    greet() {
      return 'Yo ' + firstName;
    }
  }

  ```

* Syntactic Sugar: A different way to type something that doesn't change how it works under the hood.

* **_typeof and instanceof:_**
  
  * `typeof` is an operator that returns a string with the type of whatever you pass.

  * The `typeof` operator checks if a value belongs to one of the six basic types: `number`, `string`, `boolean`, `object`, `function` or `undefined`.

  * `instanceof` is much more intelligent: it works on the level of prototypes. In particular, it tests to see if the right operand appears anywhere in the prototype chain of the left.

  ```javascript

  var a = 3;
  console.log(typeof a); // number

  var b = "Hello";
  console.log(typeof b); // string

  var c = {};
  console.log(typeof c); // object

  var d = [];
  console.log(typeof d); // object
  // Better approach
  console.log(Object.prototype.toString.call(d)); // [object Array]

  function Person(name) {
    this.name = name;
  }

  var e = new Person('Syed');
  console.log(typeof e); // object
  console.log(e instanceof Person); // true

  console.log(typeof undefined); // undefined
  console.log(typeof null); // object

  var f = function() { };
  console.log(typeof f); // function

  ```

* **_Strict Mode:_**

  It tell the javascript engine to implement some strict rules while parsing the code. Using`'use strict'` in the code enables the strict mode.

* **_Method Chaining:_**

  Calling one method after another, and each method affects the parent object. So `obj.method1().method2()`, where both methods end up with a `this` variable pointing to `obj`.

* **_Transpile:_**

  Convert the syntax of one programming language, to another.