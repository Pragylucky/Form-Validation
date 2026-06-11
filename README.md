# 📝 Vanilla JS Client-Side Form Validation

A lightweight, responsive form validation project built entirely with vanilla web technologies. This project enforces strict data formatting using Regular Expressions (Regex), provides distinct error messages for empty versus invalid fields, and includes a password visibility toggle.

## ✨ Features

* **Regex Validation:** Ensures first/last names contain only letters, emails are properly formatted, and passwords meet strict security criteria (minimum 8 characters, numbers, uppercase, lowercase, and symbols).
* **Granular Error Handling:** Differentiates between an "empty field" and an "invalid input," showing the user the exact right error message.
* **Password Visibility Toggle:** Improves user experience by allowing users to reveal or hide their typed password.
* **Success Redirect:** Once all validation flags pass, the form automatically clears its inputs and redirects to a success page.
* **Dynamic Event Tracking:** Captures keystrokes via `dataset.key` routing to update target values dynamically before submission.

## 🛠️ Tech Stack

* **HTML5:** Semantic structure and data attributes (`data-key`).
* **CSS3:** Custom styling, UI state transitions (e.g., `.d-none`, `.error`).
* **Vanilla JavaScript:** DOM traversal, event listeners, and Regular Expression matching.

## 🚧 Why This is a Foundational (Not Advanced) Project

This code is an excellent exercise in DOM manipulation and Regex, but it intentionally uses beginner-friendly patterns. In a production-level, advanced application, this codebase would be structured very differently for the following reasons:

### 1. Global Variable Pollution
The application declares many global variables (`firstName`, `lnTarget`, `fnFlag`, etc.). In a complex app, having these floating in the global scope can lead to naming collisions and bugs. Advanced projects encapsulate these inside state objects, classes, or module scopes.

### 2. Repetitive (WET) Code
The validation logic inside the `submitButton` event listener repeats the exact same `if/else` structure four times. Advanced code emphasizes being DRY (Don't Repeat Yourself) by creating a single, reusable validation function and looping through an array of field configuration objects.

### 3. Hardcoded NodeList Indices
Relying on indices like `errorMessages[0]` or `emptyfieldMessages[2]` makes the code very "brittle." If you ever added a new input field to the HTML (like a "Confirm Password" field) before the Email field, all of these index numbers would break. Advanced forms tie error messages directly to their parent inputs via IDs or targeted DOM traversal.

### 4. Input Capture Method
Relying on `keyup` to capture values into variables can miss data if a user auto-fills the form using their browser or pastes text using a mouse context menu (since no key was technically pressed). Advanced forms usually read the `value` directly from the DOM at the exact moment of submission, or use the `input` event which fires for any value change.

### 5. Lack of Type Safety
As seen with a minor typo (`flase` instead of `false`), vanilla JavaScript won't warn you about errors until the code actually runs and crashes. Advanced projects often use tools like TypeScript and linters (ESLint) to catch these bugs during the coding process.

## 🚀 Getting Started

1. Clone this repository.
2. Open `index.html` in your web browser or use VS Code's Live Server.
3. Attempt to submit the form empty, and then with various invalid inputs to test the Regex parameters.

## 👨‍💻 Author

**Lucky**
