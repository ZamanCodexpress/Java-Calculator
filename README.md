# Java Calculator
A sleek **desktop Calculator application** built using **Java and Swing**. The application replicates the look and feel of the iOS calculator — featuring a dark theme, operator highlighting, and smooth arithmetic operations — all with zero external dependencies.

---

## Overview

This is a **single-window desktop application** built entirely with Java's standard library. Users can perform everyday calculations through an intuitive button-based interface styled after Apple's native calculator.

All logic is handled in-memory, making the app lightweight, fast, and easy to run on any machine with Java installed.

---

## Features

###  Basic Arithmetic
- Addition, subtraction, multiplication, and division
- Supports multi-digit input and decimal numbers
- Displays results instantly on `=`

###  Extra Operations
- **Square Root (`√`)** — compute the root of the current display value
- **Toggle Sign (`+/-`)** — switch between positive and negative
- **Percentage (`%`)** — convert the current value to a percentage

###  Display
- Large, right-aligned number display
- Automatically removes unnecessary decimal zeros (e.g. `5.0` → `5`)
- Resets cleanly with `AC` (All Clear)

###  Styled UI
- Dark theme matching the iOS calculator aesthetic
- Color-coded buttons for quick visual recognition
- Clean, minimal layout with no visual clutter

---

## Technologies Used

- Java SE 8+
- Java Swing (`javax.swing`)
- Java AWT (`java.awt`, `java.awt.event`)

---

## Project Structure

```text
├── App.java           # Entry point — instantiates the Calculator
└── Calculator.java    # Core UI layout, button logic, and arithmetic
```

---

## Setup & Usage

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/java-calculator.git
   ```
   **OR** download the project as a `.zip` file and extract it.

2. **Compile the source files:**
   ```bash
   javac App.java Calculator.java
   ```

3. **Run the application:**
   ```bash
   java App
   ```

> No build tools, frameworks, or external libraries required.

---

## UI Layout

| Button Color  | Buttons                      |
|---------------|------------------------------|
| 🟠 Orange     | `÷`, `×`, `-`, `+`, `=`     |
| ⚪ Light Gray  | `AC`, `+/-`, `%`             |
| ⬛ Dark Gray  | `0–9`, `.`, `√`              |

The button grid uses a `GridLayout(5, 4)` and the overall frame is structured with a `BorderLayout` — display panel on top, button panel below.

---

## Implementation Details

- Two-operand arithmetic model: stores `A`, `operator`, and `B` as instance state
- `ActionListener` attached to each button handles all input events
- `removeZeroDecimal()` utility cleans up floating-point display artifacts (e.g. `4.0` → `4`)
- `clearAll()` resets operand state independently from the display label
- UI is rendered after the full button loop to ensure correct layout on startup

---

## Limitations

- No keyboard input support — mouse only
- No calculation history or memory functions
- Window is fixed size and not resizable
- Square root operates only on the current display value, not as part of a chained expression

---

## License

This project is **open-source** and intended for **educational and portfolio use**.

---

## Author

Designed and developed by **Zaman Siraj**
