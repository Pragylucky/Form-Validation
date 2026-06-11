# 🧠 Vanilla JS Trivia Quiz

A lightweight, interactive trivia application built with Vanilla JavaScript. This project fetches random questions from the Open Trivia Database API and allows users to test their knowledge, tracking their score in real-time.

## ✨ Features

* **Dynamic API Integration:** Asynchronously fetches trivia questions using `axios` from the OpenTDB API.
* **Interactive UI:** Smooth transitions between the rule book, active quiz, and final results screen.
* **Event Delegation:** Efficiently handles user clicks on dynamically generated answer buttons.
* **Real-time Scoring:** Updates the user's score immediately upon selecting an answer and visually indicates correct/incorrect choices.
* **Array Shuffling:** Randomizes the position of correct and incorrect answers so the correct choice isn't always in the same spot.

## 🛠️ Tech Stack

* **HTML5 / CSS3:** Structure and styling (utilizing utility classes like `.hide`, `.success`, `.error`).
* **Vanilla JavaScript:** Core logic, DOM manipulation, and state tracking.
* **Axios:** Promise-based HTTP client for the browser.

## 🚧 Why This is a Foundational (Not Advanced) Project

This project was built primarily as a stepping stone to master core JavaScript concepts. It intentionally avoids advanced architectural patterns, meaning there is significant room for improvement. Here is why this is considered a beginner-to-intermediate learning project:

### 1. The `setTimeout` Hack for Async Data
Currently, the app uses a hardcoded `setTimeout` of 2000ms to wait for the API data to load before rendering the first question. In an advanced application, this would be handled predictably by `await`-ing the data fetch completely and rendering a "Loading..." spinner, rather than guessing how long the network request will take.

### 2. Global State Management
Variables like `quizzes`, `currentQuestion`, and `score` are declared globally. In a larger, more advanced application, this can lead to memory leaks or data collisions. Modern apps encapsulate state within classes, modules, or state-management libraries (like Redux or React's Context).

### 3. Manual DOM Manipulation
Every UI update requires manual steps (e.g., `document.createElement`, `.appendChild`, `.innerText`). This imperative approach becomes very difficult to scale. Advanced projects use declarative frameworks (like React or Vue) or Web Components to sync the UI with the underlying data automatically.

### 4. Lack of Data Persistence
If a user refreshes the page mid-quiz, all progress and scores are completely lost. An advanced version would utilize `localStorage` or `sessionStorage` to persist the user's session.

### 5. Minor Typos in Selectors
The code relies on DOM elements with slight typos in the HTML classes (e.g., `.options-contianer`, `scoreContiner`). In an advanced environment, strict typing (like TypeScript) or component-based architecture helps prevent these UI-breaking bugs.

## 🚀 Getting Started

To run this project locally:

1. Clone this repository.
2. Ensure you have an active internet connection (required for the Axios CDN and the OpenTDB API).
3. Open `index.html` in your favorite browser.

## 👨‍💻 Author

**Lucky**
