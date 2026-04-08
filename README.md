# 📝 [My Cloud Recipe Book](https://eliandramarins.github.io/recipe-app/)



A minimalist, high-end web application for storing and managing personal recipes. This project evolved from a simple Client-Side prototype into a Secure Cloud Application integrated with Firebase.

## 🚀 Evolution of the Project
Phase 1: The Prototype (Local Storage)
Originally built as a single-page application using vanilla JavaScript.<br>

Storage: Used localStorage to save data directly in the user's browser.<br>
Features: Basic CRUD (Create, Read, Update, Delete) functionality.<br>
Limitation: Data was device-specific; clearing browser cache deleted all recipes.<br><br>

Phase 2: Cloud Integration (Firebase Firestore)<br>
Migrated the data layer from the browser's memory to the Google Cloud.<br>

Database: Integrated Firebase Firestore (NoSQL).<br>
Connectivity: Used Asynchronous JavaScript (async/await) to handle real-time data fetching.<br>
Benefit: Recipes became accessible across all devices and browsers.<br><br>

Phase 3: Security & Role-Based Access (Firebase Auth)<br>
Implemented an "Admin vs. Guest" system to protect data integrity.<br>

Authentication: Added Google Login via Firebase Auth.<br>
Authorization: Created a "Secret Admin" logic where only a specific email address (the owner) can Edit or Delete recipes.<br>
Guest Access: Public users can view and add new recipes but cannot modify existing ones.<br>
Security Rules: Hardened the database with server-side rules to prevent unauthorized API requests.<br><br>

## 🛠️ Tech Stack
Frontend: HTML5, CSS3 (Custom Properties & Flex/Grid), Vanilla JavaScript (ES6 Modules).<br>
Backend-as-a-Service: Firebase.<br>
Firestore: Real-time NoSQL Database.<br>
Authentication: Google OAuth 2.0.<br>
Hosting: GitHub Pages.<br><br>

## 🔒 Security Summary
This project utilizes a Dual-Layer Security model:<br><br>

UI Layer: Buttons for destructive actions (Edit/Delete) are hidden via JavaScript conditional rendering based on the logged-in user's email.<br>
Database Layer: Firestore Security Rules validate every request server-side, ensuring only the authenticated Admin email has update and delete permissions.
