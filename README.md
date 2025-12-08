# Overview

As a software engineer, I wanted to expand my skills in cross-platform mobile development and explore Flutter's capabilities for building real-world applications. This project allowed me to dive deeper into state management, local data persistence, and creating intuitive user interfaces that work seamlessly across multiple platforms.

**Invoice & Receipt Tracker** is a multi-platform application that helps users organize and manage their invoices and receipts. The app features two main views: an input form for adding new receipts with details like title, amount, category, date, and notes, and a comprehensive list view that displays all stored receipts sorted by date. Users can easily track their expenses, view total amounts, and delete receipts when needed. All data is automatically saved to local storage, ensuring that records persist between app sessions.

The purpose of creating this app was to gain hands-on experience with Flutter's widget system, implement persistent local storage using shared_preferences, and understand how to build applications that maintain data integrity across app restarts. This project also helped me practice JSON serialization, form validation, and creating responsive layouts that adapt to different screen sizes and platforms.

# Development Environment

**Development Tools:**
- Visual Studio Code (with Flutter and Dart extensions)
- Flutter SDK (version 3.x)
- Android Studio (for Android emulator)
- Git for version control

**Testing Platforms:**
- Android Emulator
- Chrome Browser (for web testing)
- Windows Desktop

**Programming Language:**
- Dart (Flutter's programming language)

**Libraries and Packages:**
- `flutter/material.dart` - Core Flutter UI framework with Material Design components
- `intl: ^0.18.0` - Internationalization and date formatting library
- `shared_preferences: ^2.2.2` - Local key-value storage for data persistence
- `dart:convert` - JSON encoding and decoding for data serialization

# Useful Websites

* [Flutter Official Documentation](https://docs.flutter.dev/)
* [Dart Language Tour](https://dart.dev/guides/language/language-tour)
* [Flutter Cookbook](https://docs.flutter.dev/cookbook)
* [pub.dev - Flutter Packages](https://pub.dev/)
* [Material Design 3](https://m3.material.io/)
* [SharedPreferences Documentation](https://pub.dev/packages/shared_preferences)
* [Stack Overflow - Flutter Questions](https://stackoverflow.com/questions/tagged/flutter)

# Future Work

* Add search and filter functionality to find receipts by category, date range, or amount
* Implement export feature to generate PDF or CSV reports of receipts
* Add image attachment capability to store photos of physical receipts
* Create data backup and restore functionality using cloud storage
* Implement multi-currency support with exchange rate conversion
* Add charts and analytics to visualize spending patterns by category and time period
* Enable receipt editing functionality to modify existing entries
* Add biometric authentication for securing sensitive financial data
* Implement dark mode theme option
* Add recurring receipt templates for regular expenses