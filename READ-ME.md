SoumyaBank — Simple Banking System (HTML, TailwindCSS, JavaScript)

SoumyaBank is a simple web-based banking system built to practice working with the DOM, event handling, and basic data manipulation using JavaScript.
It simulates essential banking operations such as account creation, deposits, withdrawals, and balance checks — all in a responsive interface designed with TailwindCSS.

About the Project

SoumyaBank is a single-page web application that demonstrates core JavaScript and DOM concepts.
All account data is stored temporarily in memory using JavaScript objects (no backend or database).
The interface features a clean gradient background, glassmorphism-style panels, and a modal popup for the developer’s information.

Features
1. Create a New Account

Users can create new accounts by entering their name, account number, and an initial deposit.
Each account is stored in a JavaScript dictionary.

```accounts[accNo] = { name, balance };```

2. Deposit Money

The deposit function allows users to add funds to an existing account.
It validates the account number and the entered amount before updating the balance.

```accounts[accNo].balance += amount;```

3. Withdraw Money

The withdrawal function ensures sufficient balance and validates inputs before performing the transaction.
```
if (amount <= accounts[accNo].balance) {
    accounts[accNo].balance -= amount;
}
```

4. Check Balance

Users can view their account balance instantly by entering the account number.
```
showMessage(`Account balance: ${accounts[accNo].balance}`, "green");
```
5. View All Accounts

Displays a list of all existing accounts, showing account numbers, names, and balances dynamically.
```
for (let accNo in accounts) {
    const acc = accounts[accNo];
    // Display account info in the UI
}
```
6. About Me Popup

The "About" link in the navbar opens a glassmorphic modal with a short summary about the developer.
The modal closes when the user clicks outside it or presses the close button.

Design Overview

The UI is designed using TailwindCSS and incorporates modern design principles:

Gradient background with soft color transitions

Glassmorphism effects using blurred transparency

Responsive layout for mobile and desktop

Poppins font imported from Google Fonts for a clean, modern look
```
<body class="bg-gradient-to-br from-indigo-200 via-purple-200 to-pink-200">
```
Learning Outcomes

Developing SoumyaBank helped strengthen understanding of:

JavaScript DOM manipulation

Handling user input and dynamic updates

Managing in-memory data using objects

Implementing basic form validation

Responsive and clean design using TailwindCSS

Writing modular, readable, and maintainable front-end code

How to Use

Download or clone the repository.

Open the index.html file in a web browser.

Use the navigation options to:

Create new accounts

Deposit or withdraw money

Check balances or view all accounts

Click the "About" link to open the developer information modal.

Summary

SoumyaBank is a small yet practical JavaScript project focused on learning core concepts of DOM manipulation, interactivity, and responsive UI design.
It combines logic and design to demonstrate how a simple banking interface can be built without frameworks or backend systems.
This project represents an early step in mastering front-end development and building real-world, functional web applications.