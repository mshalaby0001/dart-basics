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

 