# 🏡 Smart Home IoT System (Version 2.0)
**Mini Project #3 – Advanced Java OOP Concepts** ☕

📌 **Overview**
This project upgrades a Smart Home ecosystem to demonstrate advanced Object-Oriented Programming (OOP) concepts in Java. It features an interactive console menu, strict data encapsulation, and robust exception handling.

✅ **Concepts Covered**

**1. Encapsulation (Private variables with Getters/Setters)**
Used in `SmartDevice` (e.g., `private String deviceId`) and subclasses. Data is safely modified and accessed only through `public get/set` methods.

**2. Constructors**
Used across all classes to initialize object states (e.g., setting the initial brightness of a `SmartLight`).

**3. Inheritance using extends**
Both `SmartLight` and `SmartThermostat` use the `extends` keyword to inherit from the `SmartDevice` base class.

**4. Method Overriding**
The abstract `showStatus()` method is uniquely overridden in both the `SmartLight` and `SmartThermostat` subclasses to provide specific formatting.

**5. Polymorphism**
Demonstrated in the `SmartHub` class: `for (SmartDevice device : homeDevices) { device.showStatus(); }`. The system dynamically calls the correct subclass method at runtime.

**6. Abstraction (Abstract Class)**
`SmartDevice` is implemented as an `abstract class`. It defines a blueprint but cannot be instantiated directly.

**7. Packages**
Code is logically separated into:
*   `com.smarthome.core` (Base classes)
*   `com.smarthome.devices` (Specific devices)
*   `com.smarthome.main` (Executable entry point)

**8. Access Modifiers**
*   `private`: Variables like `brightness` and `deviceId`.
*   `public`: Methods like `getBrightness()`, classes, and constructors.

**9. Array or ArrayList**
Used an `ArrayList<SmartDevice>` to dynamically store and manage the growing list of smart home objects.

**10. User Input using Scanner**
Implemented a dynamic `Scanner` menu in `SmartHub.java` allowing the user to view devices, add new ones, and interact with the system in real-time.

**11. Exception Handling (try-catch)**
Robust error handling in `SmartHub.java`:
*   Catches `InputMismatchException` if a user types a word instead of a menu number.
*   Catches `IllegalArgumentException` if a user tries to set light brightness outside the 0-100 range.

▶️ **How to Run**

**Compile:**
```bash
javac -d out src/**/*.java
