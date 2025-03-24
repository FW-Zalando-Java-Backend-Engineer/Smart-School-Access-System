# 🚌 **Java Mini Project: Smart School Access System**

## 🎯 Objective:
Build a **Smart School Access System** in Java using **logical operators** and **ternary conditions**. The system will help manage student access to services like the **school bus**, **lunch program**, and **library**.

---

## 🧩 Project Overview:

You’ll implement 3 tasks:

1. **Student Bus Access Checker** – logical + ternary for eligibility  
2. **Lunch Eligibility Checker** – logic with multiple rules  
3. **Library Entry Gate** – nested conditions & smart responses  

Each task builds on core skills with **step-by-step guidance**.

---

## 📦 Project Structure Suggestion:
```
SmartSchoolAccess/
├── src/
│   ├── BusAccessChecker.java
│   ├── LunchEligibility.java
│   ├── LibraryGate.java
├── README.md
```

---

# ✅ Task 1: Student Bus Access Checker

### 🎯 Goal:
Create a method that checks if a student is allowed on the school bus based on age and whether they have a bus pass.

---

### 📋 Step-by-Step Instructions:
1. Create a class named `BusAccessChecker`.
2. Create a method:
   ```java
   public static String canBoardBus(int age, boolean hasBusPass)
   ```
3. Use **nested ternary operators** to implement the rules:
   - If age >= 5 AND has a pass → “Access Granted”
   - If age < 5 but has a pass → “Too Young”
   - If age >= 5 but no pass → “No Pass”
   - If underage and no pass → “Denied”

4. Call the method with different test inputs from the `main()` method.
5. Print the outputs.

---

### ✅ Example:
```java
System.out.println(canBoardBus(6, true));   // Access Granted
System.out.println(canBoardBus(4, true));   // Too Young
System.out.println(canBoardBus(7, false));  // No Pass
System.out.println(canBoardBus(3, false));  // Denied
```

---

### 📚 Resources:
- [Java Ternary Operator - W3Schools](https://www.w3schools.com/java/java_conditions.asp)  
- [Java Logical Operators - Oracle](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/opsummary.html)

---

# ✅ Task 2: Lunch Eligibility Checker

### 🎯 Goal:
Build a system that determines if a student is eligible for a free lunch based on:
- **Has lunch pass** OR is **under 12**
- If neither is true, they must pay

---

### 📋 Step-by-Step Instructions:
1. Create a class `LunchEligibility`.
2. Create a method:
   ```java
   public static String checkLunchAccess(boolean hasLunchPass, int age)
   ```
3. Use **logical operators**:
   - If hasLunchPass OR age < 12 → "Free Lunch"
   - Else → "Paid Lunch"

4. Test multiple scenarios using `main()`.

---

### ✅ Example:
```java
System.out.println(checkLunchAccess(true, 15));  // Free Lunch
System.out.println(checkLunchAccess(false, 10)); // Free Lunch
System.out.println(checkLunchAccess(false, 14)); // Paid Lunch
```

---

### 📚 Resources:
- [Logical Operators - GeeksForGeeks](https://www.geeksforgeeks.org/logical-operators-in-java/)  
- [Booleans & Conditions - JavaPoint](https://www.javatpoint.com/java-if-else)

---

# ✅ Task 3: Library Entry Gate

### 🎯 Goal:
Simulate an intelligent library gate that decides:
- If a student has a **library card**
- If they are **late** (entry only before 4:00 PM)

---

### 📋 Step-by-Step Instructions:
1. Create a class `LibraryGate`.
2. Create a method:
   ```java
   public static String canEnterLibrary(boolean hasLibraryCard, int hour)
   ```
3. Use **logical AND (`&&`)** and **ternary operators** to implement:
   - If hasLibraryCard AND hour < 16 → “Welcome to the Library”
   - If no card → “No Library Card”
   - If too late → “Library Closed for Students”

---

### ✅ Example:
```java
System.out.println(canEnterLibrary(true, 15));  // Welcome to the Library
System.out.println(canEnterLibrary(false, 14)); // No Library Card
System.out.println(canEnterLibrary(true, 17));  // Library Closed for Students
```

---

### 📚 Resources:
- [Java Nested Ternary Operators - TutorialsPoint](https://www.tutorialspoint.com/java/java_basic_operators.htm)  
- [Java Conditions Best Practices - Baeldung](https://www.baeldung.com/java-ternary-operator)

---

## 🧠 Bonus Challenge (Optional):
Add a **combined dashboard class** that:
- Accepts **all student info**
- Calls all 3 checkers
- Prints a final access report for the student

---
