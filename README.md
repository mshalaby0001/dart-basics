# dart_basics

Here’s a rewritten version of your answer, incorporating **code examples** for each concept:

---

## Variables 

### **Variable Declaration**
Dart supports variables declared with `var`, `dynamic`, `final`, and `const`.

#### 1. **`var` (Type Inference)**
`var` infers the type from the initial value.
```dart
var name = 'Alice'; // Dart infers the type as String
var age = 25;       // Dart infers the type as int
print(name);        // Output: Alice
print(age);         // Output: 25
```

#### 2. **`dynamic` (Flexible Typing)**
`dynamic` allows the variable to hold any type and can change over time.
```dart
dynamic value = 'Hello'; // Can hold any type
value = 100;             // Now it's an int
value = true;            // Now it's a bool
print(value);            // Output: true
```

#### 3. **`final` (Immutable After Initialization)**
`final` variables can be set only once and are immutable after initialization.
```dart
final String greeting = 'Hello, Dart!';
// greeting = 'Hi'; // Error: 'final' variables cannot be reassigned
print(greeting);    // Output: Hello, Dart!
```

#### 4. **`const` (Compile-Time Constants)**
`const` variables are compile-time constants and are also immutable.
```dart
const double pi = 3.14159;
// pi = 3.14; // Error: 'const' variables cannot be reassigned
print(pi);    // Output: 3.14159
```

---

### **Type Safety**
Dart is type-safe, meaning the type of a variable is known at compile time. However, you can use `dynamic` to bypass this if needed.
```dart
String name = 'Bob'; // Explicitly typed as String
// name = 42; // Error: A value of type 'int' can't be assigned to a variable of type 'String'

dynamic value = 'Hello'; // Bypassing type safety
value = 100; // Allowed because 'dynamic' can hold any type
```

---

### **Default Values**
Uninitialized variables have a default value of `null`, even for numeric types.
```dart
int? uninitialized; // Declared but not initialized
print(uninitialized); // Output: null
```

---

### **`final` vs `const`**
- **`final`**: Used for variables that won’t change after initialization (can be set at runtime).
- **`const`**: Used for compile-time constants (must be known at compile time).

#### Example of `final`:
```dart
final DateTime now = DateTime.now(); // Runtime initialization
print(now); // Output: Current date and time
```

#### Example of `const`:
```dart
const List<int> numbers = [1, 2, 3]; // Compile-time constant
// numbers.add(4); // Error: 'const' lists are immutable
print(numbers); // Output: [1, 2, 3]
```

---

### **Type Inference**
Dart can infer types when `var` is used, making the code cleaner.
```dart
var message = 'Hello, Dart!'; // Dart infers the type as String
var count = 42;               // Dart infers the type as int
print(message);               // Output: Hello, Dart!
print(count);                 // Output: 42
```

---

### **Examples of Variable Modifiers**
Here’s a summary of variable declarations with different modifiers:
```dart
var inferred = 'Dart';       // Inferred as String
dynamic flexible = 'Hello';  // Can change type
final immutable = 100;       // Cannot be reassigned
const constant = 3.14;       // Compile-time constant

print(inferred);   // Output: Dart
print(flexible);   // Output: Hello
print(immutable);  // Output: 100
print(constant);   // Output: 3.14
```

---

## Built-in types

Here’s a summary of the [Dart Built-in Types](https://dart.dev/language/built-in-types) page, using the same method with explanations and **code examples**:

---

### **Dart Built-in Types**
Dart provides several built-in types, including numbers, strings, booleans, lists, sets, maps, and more.

---

### **1. Numbers**
Dart supports two types of numbers: `int` (integers) and `double` (floating-point numbers).

#### Example:
```dart
int age = 25;          // Integer
double height = 5.9;   // Double
print(age);            // Output: 25
print(height);         // Output: 5.9
```

---

### **2. Strings**
Strings are sequences of characters and can be enclosed in single or double quotes.

#### Example:
```dart
String name = 'Alice';
String greeting = "Hello, $name!"; // String interpolation
print(greeting); // Output: Hello, Alice!
```

---

### **3. Booleans**
Booleans represent true or false values.

#### Example:
```dart
bool isRaining = true;
bool isSunny = false;
print(isRaining); // Output: true
```

---

### **4. Lists**
Lists are ordered collections of objects. They can be fixed-length or growable.

#### Example:
```dart
List<int> numbers = [1, 2, 3]; // Growable list
numbers.add(4);                // Add an element
print(numbers);                // Output: [1, 2, 3, 4]
```

---

### **5. Sets**
Sets are unordered collections of unique items.

#### Example:
```dart
Set<String> fruits = {'apple', 'banana', 'orange'};
fruits.add('apple'); // Duplicate item, won't be added
print(fruits);       // Output: {apple, banana, orange}
```

---

### **6. Maps**
Maps are collections of key-value pairs.

#### Example:
```dart
Map<String, int> ages = {
  'Alice': 25,
  'Bob': 30,
};
print(ages['Alice']); // Output: 25
```

---

### **7. Runes**
Runes represent Unicode code points of a string.

#### Example:
```dart
var heart = '\u2665'; // Unicode for a heart symbol
print(heart);         // Output: ♥
```

---

### **8. Symbols**
Symbols are used to represent identifiers or metadata.

#### Example:
```dart
var symbol = #mySymbol; // Symbol literal
print(symbol);          // Output: Symbol("mySymbol")
```

---

### **9. Null**
Dart has a special type `Null` to represent the absence of a value.

#### Example:
```dart
int? nullableValue; // Nullable integer
print(nullableValue); // Output: null
```

---

### **10. Type Inference**
Dart can infer types automatically when you use `var`.

#### Example:
```dart
var message = 'Hello'; // Inferred as String
var count = 42;        // Inferred as int
print(message);        // Output: Hello
print(count);          // Output: 42
```

---

### **11. Type Checking**
You can check the type of a variable at runtime using `is` and `is!`.

#### Example:
```dart
var value = 42;
print(value is int);  // Output: true
print(value is! String); // Output: true
```

---

### **12. Type Casting**
You can cast objects to a specific type using the `as` keyword.

#### Example:
```dart
num number = 42;
int integer = number as int; // Casting to int
print(integer);              // Output: 42
```

---

### **Summary of Built-in Types**
| Type      | Example                          |
|-----------|----------------------------------|
| `int`     | `int age = 25;`                  |
| `double`  | `double height = 5.9;`           |
| `String`  | `String name = 'Alice';`         |
| `bool`    | `bool isRaining = true;`         |
| `List`    | `List<int> numbers = [1, 2, 3];` |
| `Set`     | `Set<String> fruits = {'apple'};`|
| `Map`     | `Map<String, int> ages = {'Alice': 25};` |
| `Runes`   | `var heart = '\u2665';`          |
| `Symbol`  | `var symbol = #mySymbol;`        |
| `Null`    | `int? nullableValue;`            |

---

 ## Functions 

Here’s a summary of the [Dart Functions](https://dart.dev/language/functions) page, using the same method with explanations and **code examples**:

---

### **Dart Functions**
Functions are reusable blocks of code that perform a specific task. Dart supports various types of functions, including named parameters, optional parameters, and arrow syntax.

---

### **1. Basic Function**
A simple function that takes parameters and returns a value.

#### Example:
```dart
int add(int a, int b) {
  return a + b;
}
print(add(2, 3)); // Output: 5
```

---

### **2. Arrow Syntax**
For single-expression functions, you can use the arrow (`=>`) syntax.

#### Example:
```dart
int multiply(int a, int b) => a * b;
print(multiply(2, 3)); // Output: 6
```

---

### **3. Optional Parameters**
Dart supports optional positional and named parameters.

#### **a. Optional Positional Parameters**
Use square brackets `[]` to define optional positional parameters.

#### Example:
```dart
String greet(String name, [String? title]) {
  return title == null ? 'Hello, $name!' : 'Hello, $title $name!';
}
print(greet('Alice'));           // Output: Hello, Alice!
print(greet('Bob', 'Mr.'));      // Output: Hello, Mr. Bob!
```

#### **b. Optional Named Parameters**
Use curly braces `{}` to define optional named parameters.

#### Example:
```dart
String greet({String? name, String? title}) {
  return title == null ? 'Hello, $name!' : 'Hello, $title $name!';
}
print(greet(name: 'Alice'));           // Output: Hello, Alice!
print(greet(title: 'Mr.', name: 'Bob')); // Output: Hello, Mr. Bob!
```

---

### **4. Default Parameter Values**
You can provide default values for optional parameters.

#### Example:
```dart
String greet({String name = 'Guest', String title = 'Mr.'}) {
  return 'Hello, $title $name!';
}
print(greet()); // Output: Hello, Mr. Guest!
```

---

### **5. Anonymous Functions**
Anonymous functions (or lambdas) are functions without a name.

#### Example:
```dart
var list = [1, 2, 3];
list.forEach((item) {
  print(item); // Output: 1, 2, 3
});
```

---

### **6. Lexical Scope**
Dart is lexically scoped, meaning the scope of variables is determined by the layout of the code.

#### Example:
```dart
var x = 10;
void printX() {
  print(x); // Accessing the outer variable
}
printX(); // Output: 10
```

---

### **7. Lexical Closures**
Functions can capture and retain variables from their surrounding scope.

#### Example:
```dart
Function makeAdder(int addBy) {
  return (int i) => addBy + i;
}
var addTwo = makeAdder(2);
print(addTwo(3)); // Output: 5
```

---

### **8. `main()` Function**
The `main()` function is the entry point of a Dart program.

#### Example:
```dart
void main() {
  print('Hello, Dart!'); // Output: Hello, Dart!
}
```

---

### **9. Functions as First-Class Objects**
Functions can be assigned to variables, passed as arguments, and returned from other functions.

#### Example:
```dart
void printMessage(String message) {
  print(message);
}

void main() {
  var showMessage = printMessage; // Assigning a function to a variable
  showMessage('Hello, Dart!');    // Output: Hello, Dart!
}
```

---

### **10. Generators**
Generators produce a sequence of values lazily using `sync*` and `async*`.

#### Example:
```dart
Iterable<int> generateNumbers(int n) sync* {
  for (var i = 1; i <= n; i++) {
    yield i;
  }
}

void main() {
  var numbers = generateNumbers(3);
  print(numbers.toList()); // Output: [1, 2, 3]
}
```

---

### **Summary of Dart Functions**
| Feature                     | Example                                                                 |
|-----------------------------|-------------------------------------------------------------------------|
| Basic Function              | `int add(int a, int b) { return a + b; }`                               |
| Arrow Syntax                | `int multiply(int a, int b) => a * b;`                                  |
| Optional Positional Params  | `String greet(String name, [String? title]) { ... }`                    |
| Optional Named Params       | `String greet({String? name, String? title}) { ... }`                   |
| Default Parameter Values    | `String greet({String name = 'Guest', String title = 'Mr.'}) { ... }`   |
| Anonymous Functions         | `list.forEach((item) { print(item); });`                                |
| Lexical Scope               | `var x = 10; void printX() { print(x); }`                               |
| Lexical Closures            | `Function makeAdder(int addBy) { return (int i) => addBy + i; }`        |
| `main()` Function           | `void main() { print('Hello, Dart!'); }`                                |
| Functions as First-Class    | `var showMessage = printMessage; showMessage('Hello, Dart!');`          |
| Generators                  | `Iterable<int> generateNumbers(int n) sync* { for (var i = 1; i <= n; i++) yield i; }` |

---

## Operators 

Here’s a summary of the [Dart Operators](https://dart.dev/language/operators) page, using the same method with explanations and **code examples**:

---

### **Dart Operators**
Dart provides a variety of operators for performing operations on variables and values. These include arithmetic, equality, relational, logical, and more.

---

### **1. Arithmetic Operators**
Used for basic mathematical operations.

| Operator | Description          | Example                     |
|----------|----------------------|-----------------------------|
| `+`      | Addition             | `print(2 + 3); // 5`        |
| `-`      | Subtraction          | `print(5 - 2); // 3`        |
| `*`      | Multiplication       | `print(2 * 3); // 6`        |
| `/`      | Division             | `print(6 / 3); // 2.0`      |
| `%`      | Modulus (Remainder)  | `print(7 % 3); // 1`        |
| `~/`     | Integer Division     | `print(7 ~/ 3); // 2`       |
| `-expr`  | Negation             | `print(-(5)); // -5`        |

---

### **2. Equality and Relational Operators**
Used to compare values.

| Operator | Description                  | Example                         |
|----------|------------------------------|---------------------------------|
| `==`     | Equal to                     | `print(2 == 3); // false`       |
| `!=`     | Not equal to                 | `print(2 != 3); // true`        |
| `>`      | Greater than                 | `print(5 > 3); // true`         |
| `<`      | Less than                    | `print(5 < 3); // false`        |
| `>=`     | Greater than or equal to     | `print(5 >= 5); // true`        |
| `<=`     | Less than or equal to        | `print(5 <= 3); // false`       |

---

### **3. Logical Operators**
Used to combine boolean expressions.

| Operator | Description                  | Example                                   |
|----------|------------------------------|-------------------------------------------|
| `&&`     | Logical AND                  | `print(true && false); // false`          |
| `||`     | Logical OR                   | `print(true || false); // true`           |
| `!`      | Logical NOT                  | `print(!true); // false`                  |

---

### **4. Type Test Operators**
Used to check the type of an object.

| Operator | Description                  | Example                                   |
|----------|------------------------------|-------------------------------------------|
| `is`     | True if the object has the specified type | `print(5 is int); // true`          |
| `is!`    | True if the object does not have the specified type | `print(5 is! String); // true` |

---

### **5. Assignment Operators**
Used to assign values to variables.

| Operator | Description                  | Example                                   |
|----------|------------------------------|-------------------------------------------|
| `=`      | Simple assignment            | `var x = 5;`                              |
| `+=`     | Add and assign               | `x += 3; // x = x + 3`                    |
| `-=`     | Subtract and assign          | `x -= 2; // x = x - 2`                    |
| `*=`     | Multiply and assign          | `x *= 2; // x = x * 2`                    |
| `/=`     | Divide and assign            | `x /= 2; // x = x / 2`                    |
| `%=`     | Modulus and assign           | `x %= 2; // x = x % 2`                    |
| `~/=`    | Integer division and assign  | `x ~/= 2; // x = x ~/ 2`                  |

---

### **6. Conditional Expressions**
Used for conditional evaluation.

| Operator | Description                  | Example                                   |
|----------|------------------------------|-------------------------------------------|
| `expr1 ? expr2 : expr3` | Ternary operator | `print(5 > 3 ? 'Yes' : 'No'); // Yes` |
| `expr1 ?? expr2`        | Null-coalescing operator | `var x = null; print(x ?? 10); // 10` |

---

### **7. Cascade Notation (`..`)**
Allows you to perform multiple operations on the same object.

#### Example:
```dart
class Person {
  String? name;
  int? age;

  void printInfo() {
    print('Name: $name, Age: $age');
  }
}

void main() {
  var person = Person()
    ..name = 'Alice'
    ..age = 25
    ..printInfo(); // Output: Name: Alice, Age: 25
}
```

---

### **8. Bitwise and Shift Operators**
Used for low-level bit manipulation.

| Operator | Description                  | Example                                   |
|----------|------------------------------|-------------------------------------------|
| `&`      | Bitwise AND                  | `print(5 & 3); // 1`                     |
| `|`      | Bitwise OR                   | `print(5 | 3); // 7`                     |
| `^`      | Bitwise XOR                  | `print(5 ^ 3); // 6`                      |
| `~`      | Bitwise NOT                  | `print(~5); // -6`                        |
| `<<`     | Left shift                   | `print(5 << 1); // 10`                    |
| `>>`     | Right shift                  | `print(5 >> 1); // 2`                     |

---

### **9. Other Operators**
| Operator | Description                  | Example                                   |
|----------|------------------------------|-------------------------------------------|
| `?.`     | Conditional access           | `var obj; print(obj?.name); // null`      |
| `[]`     | Access list/map element      | `var list = [1, 2]; print(list[0]); // 1` |
| `()`     | Function call                | `void greet() { print('Hello'); } greet();` |

---

### **Summary of Dart Operators**
| Category                  | Example                                   |
|---------------------------|-------------------------------------------|
| Arithmetic                | `print(2 + 3); // 5`                     |
| Equality/Relational       | `print(2 == 3); // false`                 |
| Logical                   | `print(true && false); // false`          |
| Type Test                 | `print(5 is int); // true`                |
| Assignment                | `x += 3; // x = x + 3`                    |
| Conditional Expressions   | `print(5 > 3 ? 'Yes' : 'No'); // Yes`     |
| Cascade Notation          | `person..name = 'Alice'..age = 25;`       |
| Bitwise/Shift             | `print(5 & 3); // 1`                      |
| Other                     | `print(obj?.name); // null`               |

---
## Control Flow Statments 

Here’s a summary of the [Dart Branches](https://dart.dev/language/branches) page, using the same method with explanations and **code examples**:

---

### **Dart Branches**
Dart provides control flow statements like `if`, `else`, `switch`, and `case` to handle decision-making in your code.

---

### **1. `if` and `else` Statements**
Used to execute code based on a condition.

#### Example:
```dart
int age = 18;
if (age >= 18) {
  print('You are an adult.');
} else {
  print('You are a minor.');
}
// Output: You are an adult.
```

---

### **2. `else if` Ladder**
Used to check multiple conditions.

#### Example:
```dart
int score = 85;
if (score >= 90) {
  print('Grade: A');
} else if (score >= 80) {
  print('Grade: B');
} else if (score >= 70) {
  print('Grade: C');
} else {
  print('Grade: F');
}
// Output: Grade: B
```

---

### **3. `switch` and `case` Statements**
Used to compare a value against multiple cases.

#### Example:
```dart
String day = 'Monday';
switch (day) {
  case 'Monday':
    print('Start of the workweek.');
    break;
  case 'Friday':
    print('End of the workweek.');
    break;
  default:
    print('Midweek day.');
}
// Output: Start of the workweek.
```

---

### **4. `break` and `continue`**
- `break`: Exits the loop or switch statement.
- `continue`: Skips the current iteration and moves to the next.

#### Example:
```dart
for (var i = 0; i < 5; i++) {
  if (i == 2) {
    continue; // Skip iteration when i is 2
  }
  if (i == 4) {
    break; // Exit loop when i is 4
  }
  print(i);
}
// Output: 0, 1, 3
```

---

### **5. `assert` Statement**
Used to check for conditions during development. If the condition is false, it throws an error.

#### Example:
```dart
int age = 15;
assert(age >= 18, 'Age must be 18 or older.'); // Throws an error in debug mode
```

---

### **6. Ternary Operator (`? :`)**
A shorthand for `if-else` statements.

#### Example:
```dart
int age = 20;
String status = age >= 18 ? 'Adult' : 'Minor';
print(status); // Output: Adult
```

---

### **7. `for` Loop**
Used to iterate over a sequence of values.

#### Example:
```dart
for (var i = 0; i < 3; i++) {
  print(i);
}
// Output: 0, 1, 2
```

---

### **8. `while` Loop**
Repeats a block of code while a condition is true.

#### Example:
```dart
int i = 0;
while (i < 3) {
  print(i);
  i++;
}
// Output: 0, 1, 2
```

---

### **9. `do-while` Loop**
Similar to `while`, but the condition is checked after the loop body.

#### Example:
```dart
int i = 0;
do {
  print(i);
  i++;
} while (i < 3);
// Output: 0, 1, 2
```

---

### **10. `for-in` Loop**
Used to iterate over elements in a collection.

#### Example:
```dart
var numbers = [1, 2, 3];
for (var number in numbers) {
  print(number);
}
// Output: 1, 2, 3
```

---

### **11. `break` and `continue` in Loops**
- `break`: Exits the loop.
- `continue`: Skips the current iteration.

#### Example:
```dart
for (var i = 0; i < 5; i++) {
  if (i == 2) continue; // Skip iteration when i is 2
  if (i == 4) break;    // Exit loop when i is 4
  print(i);
}
// Output: 0, 1, 3
```

---

### **Summary of Dart Branches**
| Feature               | Example                                   |
|-----------------------|-------------------------------------------|
| `if-else`             | `if (age >= 18) { print('Adult'); }`      |
| `else if`             | `else if (score >= 80) { print('B'); }`   |
| `switch-case`         | `switch (day) { case 'Monday': ... }`     |
| `break`               | `break;`                                  |
| `continue`            | `continue;`                               |
| `assert`              | `assert(age >= 18, 'Age must be 18+');`   |
| Ternary Operator      | `status = age >= 18 ? 'Adult' : 'Minor';` |
| `for` Loop            | `for (var i = 0; i < 3; i++) { ... }`     |
| `while` Loop          | `while (i < 3) { ... }`                   |
| `do-while` Loop       | `do { ... } while (i < 3);`               |
| `for-in` Loop         | `for (var number in numbers) { ... }`     |

---

Here’s a summary of the [Dart Loops](https://dart.dev/language/loops) page, using the same method with explanations and **code examples**:

---

### **Dart Loops**
Loops are used to repeatedly execute a block of code. Dart supports several types of loops, including `for`, `while`, `do-while`, and `for-in`.

---

### **1. `for` Loop**
The `for` loop is used to iterate a block of code a specific number of times.

#### Example:
```dart
for (var i = 0; i < 3; i++) {
  print(i);
}
// Output: 0, 1, 2
```

---

### **2. `while` Loop**
The `while` loop repeats a block of code as long as a condition is true.

#### Example:
```dart
var i = 0;
while (i < 3) {
  print(i);
  i++;
}
// Output: 0, 1, 2
```

---

### **3. `do-while` Loop**
The `do-while` loop is similar to the `while` loop, but the condition is evaluated after the loop body, ensuring the loop runs at least once.

#### Example:
```dart
var i = 0;
do {
  print(i);
  i++;
} while (i < 3);
// Output: 0, 1, 2
```

---

### **4. `for-in` Loop**
The `for-in` loop is used to iterate over elements in a collection (e.g., lists, sets).

#### Example:
```dart
var numbers = [1, 2, 3];
for (var number in numbers) {
  print(number);
}
// Output: 1, 2, 3
```

---

### **5. `break` Statement**
The `break` statement is used to exit a loop prematurely.

#### Example:
```dart
for (var i = 0; i < 5; i++) {
  if (i == 3) {
    break; // Exit the loop when i is 3
  }
  print(i);
}
// Output: 0, 1, 2
```

---

### **6. `continue` Statement**
The `continue` statement skips the current iteration and moves to the next iteration of the loop.

#### Example:
```dart
for (var i = 0; i < 5; i++) {
  if (i == 2) {
    continue; // Skip iteration when i is 2
  }
  print(i);
}
// Output: 0, 1, 3, 4
```

---

### **7. Nested Loops**
Loops can be nested inside other loops.

#### Example:
```dart
for (var i = 1; i <= 2; i++) {
  for (var j = 1; j <= 2; j++) {
    print('i: $i, j: $j');
  }
}
// Output:
// i: 1, j: 1
// i: 1, j: 2
// i: 2, j: 1
// i: 2, j: 2
```

---

### **8. Iterating Over Maps**
You can use `for-in` loops to iterate over keys, values, or entries in a map.

#### Example:
```dart
var ages = {'Alice': 25, 'Bob': 30};
for (var name in ages.keys) {
  print('Name: $name');
}
// Output:
// Name: Alice
// Name: Bob

for (var age in ages.values) {
  print('Age: $age');
}
// Output:
// Age: 25
// Age: 30

for (var entry in ages.entries) {
  print('${entry.key}: ${entry.value}');
}
// Output:
// Alice: 25
// Bob: 30
```

---

### **9. `forEach` Method**
The `forEach` method is a concise way to iterate over collections.

#### Example:
```dart
var numbers = [1, 2, 3];
numbers.forEach((number) {
  print(number);
});
// Output: 1, 2, 3
```

---

### **10. `for` Loop with Iterables**
You can use `for` loops with iterables like lists, sets, and maps.

#### Example:
```dart
var fruits = {'apple', 'banana', 'orange'};
for (var fruit in fruits) {
  print(fruit);
}
// Output: apple, banana, orange
```

---

### **Summary of Dart Loops**
| Loop Type       | Example                                   |
|-----------------|-------------------------------------------|
| `for`           | `for (var i = 0; i < 3; i++) { ... }`     |
| `while`         | `while (i < 3) { ... }`                   |
| `do-while`      | `do { ... } while (i < 3);`               |
| `for-in`        | `for (var number in numbers) { ... }`     |
| `break`         | `if (i == 3) break;`                      |
| `continue`      | `if (i == 2) continue;`                   |
| Nested Loops    | `for (var i = 1; i <= 2; i++) { ... }`    |
| Iterating Maps  | `for (var entry in ages.entries) { ... }` |
| `forEach`       | `numbers.forEach((number) { ... });`      |

---

