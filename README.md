# dart_basics

Here’s a rewritten version of your answer, incorporating **code examples** for each concept:

---

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

This version combines explanations with **code examples** to make the concepts clearer. Let me know if you need further clarification!