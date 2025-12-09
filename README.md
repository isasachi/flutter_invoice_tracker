# Overview

As a software engineer, I wanted to expand my skills in cross-platform mobile development and explore Flutter's capabilities for building real-world applications with cloud integration. This project allowed me to dive deeper into state management, cloud-based data persistence, user authentication, and creating intuitive user interfaces that work seamlessly across multiple platforms.

**Invoice & Receipt Tracker** is a multi-platform application that helps users organize and manage their invoices and receipts securely in the cloud. The app features a complete authentication system with both email/password and Google Sign-In options, ensuring each user's data remains private and accessible from any device. Once authenticated, users can access two main views: an input form for adding new receipts with details like title, amount, category, date, and notes, and a comprehensive list view that displays all stored receipts sorted by date. Users can easily track their expenses, view total amounts, and delete receipts when needed. All data is automatically synchronized with Firebase Firestore in real-time, ensuring that records are securely stored in the cloud and accessible across all user devices.

The purpose of creating this app was to gain hands-on experience with Flutter's widget system, implement cloud-based authentication and data storage using Firebase, and understand how to build secure, multi-user applications that synchronize data in real-time. This project also helped me practice Firebase integration, user authentication flows, Firestore database design with security rules, JSON serialization, form validation, and creating responsive layouts that adapt to different screen sizes and platforms.

# Development Environment

**Development Tools:**
- Visual Studio Code (with Flutter and Dart extensions)
- Flutter SDK (version 3.x)
- Android Studio (for Android emulator)
- Firebase Console (for backend configuration)
- Git for version control

**Testing Platforms:**
- Android Emulator
- Chrome Browser (for web testing)
- Windows Desktop

**Programming Language:**
- Dart (Flutter's programming language)

**Libraries and Packages:**
- `flutter/material.dart` - Core Flutter UI framework with Material Design components
- `intl: ^0.20.0` - Internationalization and date formatting library
- `firebase_core: ^3.7.0` - Firebase SDK core functionality
- `firebase_auth: ^5.3.1` - Firebase Authentication for user management
- `cloud_firestore: ^5.6.12` - Cloud Firestore NoSQL database for data storage
- `google_sign_in: ^6.1.5` - Google Sign-In integration for OAuth authentication

**Backend Services:**
- Firebase Authentication - Manages user sign-up, login, and session handling
- Cloud Firestore - NoSQL database storing receipt data with real-time synchronization
- Firebase Security Rules - Server-side validation ensuring users can only access their own data

# Firebase Architecture

**Authentication System:**
The app implements a dual authentication approach allowing users to sign in via email/password or Google OAuth. Firebase Authentication handles all user management, session tokens, and security. An `AuthWrapper` widget listens to authentication state changes and automatically routes users to the login page or home page based on their authentication status.

**Database Structure:**
Firestore stores receipts in a `receipts` collection where each document contains:
- `title` (string) - Receipt description
- `amount` (number) - Transaction amount
- `date` (timestamp) - Receipt date
- `category` (string) - Expense category
- `notes` (string) - Additional information
- `userId` (string) - Links receipt to the authenticated user
- `createdAt` (timestamp) - Server timestamp for record creation

**Security Implementation:**
Firestore security rules ensure data privacy by:
- Requiring authentication for all database operations
- Restricting users to only read/write their own receipts (matching userId)
- Validating that created receipts have the correct userId field
- Preventing unauthorized access to other users' data

**Real-time Synchronization:**
The app uses Firestore's `StreamBuilder` widget to listen for real-time updates, automatically refreshing the UI whenever data changes in the cloud. This enables seamless multi-device synchronization where receipts added on one device instantly appear on all other logged-in devices.

# Useful Websites

* [Flutter Official Documentation](https://docs.flutter.dev/)
* [Dart Language Tour](https://dart.dev/guides/language/language-tour)
* [Flutter Cookbook](https://docs.flutter.dev/cookbook)
* [pub.dev - Flutter Packages](https://pub.dev/)
* [Firebase Documentation](https://firebase.google.com/docs)
* [Firebase Console](https://console.firebase.google.com/)
* [FlutterFire Documentation](https://firebase.flutter.dev/)
* [Cloud Firestore Documentation](https://firebase.google.com/docs/firestore)
* [Firebase Authentication Documentation](https://firebase.google.com/docs/auth)
* [Material Design 3](https://m3.material.io/)
* [Google Sign-In for Flutter](https://pub.dev/packages/google_sign_in)
* [Stack Overflow - Flutter Questions](https://stackoverflow.com/questions/tagged/flutter)
* [Stack Overflow - Firebase Questions](https://stackoverflow.com/questions/tagged/firebase)

# Future Work

* Add search and filter functionality to find receipts by category, date range, or amount
* Implement export feature to generate PDF or CSV reports of receipts with Firebase Storage integration
* Add image attachment capability using Firebase Storage to store photos of physical receipts
* Create automatic cloud backup with Firebase Storage and implement data export/import functionality
* Implement multi-currency support with exchange rate conversion using real-time APIs
* Add charts and analytics using Firebase Analytics to visualize spending patterns by category and time period
* Enable receipt editing functionality to modify existing entries with audit trails
* Add biometric authentication for securing sensitive financial data while maintaining Firebase session
* Implement dark mode theme option with user preference sync via Firestore
* Add recurring receipt templates for regular expenses stored in user's Firestore profile
* Implement offline mode with local caching and automatic sync when connection is restored
* Add push notifications using Firebase Cloud Messaging for receipt reminders and spending alerts
* Create shared receipt collections for household expense tracking with multiple users
* Implement receipt scanning with OCR using Firebase ML Kit to auto-populate fields from photos
* Add budget tracking and spending limits with Firebase Cloud Functions for server-side calculations