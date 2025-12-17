# Cataku - Finance Tracker 💰

💰
![Android](https://img.shields.io/badge/Platform-Android-green)
![Status](https://img.shields.io/badge/Status-Production-blue)
![Architecture](https://img.shields.io/badge/Architecture-Clean_Architecture-orange)

> **A production-ready personal finance tracker built with an Offline-First approach.**

---

## 📱 Project Philosophy: Radical Simplicity

**Cataku** was built with a singular goal: **Zero-Friction Financial Tracking.**

While many modern apps suffer from feature bloat and complex UIs, this project strictly adheres to **Minimalist Design Principles**. The interface is intentionally stripped down to ensure usability across all demographics—from tech-savvy Gen Z to elderly users who need large, clear touch targets without distractions.

**Why this matters:**

- **Cognitive Load Reduction:** Users can log transactions in < 3 seconds.
- **Universal Accessibility:** High contrast and simple navigation make it usable for non-digital natives.
- **Performance:** The lightweight UI logic (powered by NativeWind) ensures instant rendering even on low-end devices.

**[GOOGLE PLAYSTORE](https://play.google.com/store/apps/details?id=com.barqidev.app&hl=id)**

---

## 🚀 Key Features

### 1. Dynamic Category Management (New Implementation)

To provide granular financial insights, I implemented a flexible categorization system allowing users to define their own financial taxonomy.

- **CRUD Operations:** Users can Create, Rename, and Delete custom categories (e.g., "Salary", "Groceries", "Entertainment").
- **Relational Mapping:** Transactions are loosely coupled with categories, allowing for nullable assignment.
- **Aggregated Insights:** The system generates summaries based on these user-defined categories to visualize spending habits.

### 2. Core Functionalities

- **Expense & Income Tracking:** Rapid data entry optimized for minimal user friction.
- **Offline Capability:** Fully functional without an internet connection using a local embedded database.
- **Data Privacy:** All financial data resides on the user's device.

---

## 🛠 Technical Stack & Architecture

This project was built to demonstrate **scalable mobile architecture** and **robust data handling**.

### 📱 Mobile Client (Android)

The mobile client is built on the bleeding edge of the React Native ecosystem.

- **Core Framework:** `React Native 0.76` (Leveraging the performance improvements).
- **Language:** `TypeScript` (Strict typing for maintainability).
- **State Management:** `Recoil` (Atomic state management for granular re-renders and high performance).
- **Styling:** `NativeWind` + `TailwindCSS` (Utility-first styling for consistent design systems).
- **Navigation:** `React Navigation 7` ( Routing).
- **Storage:** `@react-native-async-storage` (Persisting user preferences).
- **Animations:** `react-native-reanimated` (60fps declarative animations).
- **Quality Assurance:** `Jest` + `@testing-library/react-native` (Unit & Integration testing).

### 🔙 Backend API (The Core)

- **Language:** PHP 8.2
- **Framework:** Laravel 12
- **Authentication:** Laravel Sanctum (Secure Token-Based Auth)
- **Quality Assurance:** PHP CS Fixer & PHPUnit
- **SEO/Indexing:** Spatie Laravel Sitemap
- **Database:** Postgresql with Relational Schema with Eloquent ORM

---

## 💡 Key Engineering Decisions

### 1. Infrastructure-Driven Refactoring (Node.js ➡️ Laravel)

Initially, the backend was developed using **Node.js**. However, during the deployment phase, I encountered compatibility constraints with the target hosting infrastructure (Shared environment) which was not optimized for long-running Node processes.

**The Solution:**
Instead of forcing an incompatible stack, I made the strategic decision to **migrate and rewrite the backend using Laravel (PHP 8.2)**.

- **Infrastructure Alignment:** PHP is natively supported by the hosting environment, ensuring higher stability and zero downtime without complex process management.
- **Development Velocity:** Leveraging Laravel's ecosystem (Sanctum, Eloquent) allowed me to rapidly port the business logic while maintaining strict type safety.
- **Future-Proofing:** The move to Laravel 12 ensures the system runs on the latest, most secure framework version available.

### 2. Adopting React Native 0.76 (New Architecture)

I deliberately upgraded the codebase to **React Native 0.76** to align with the latest industry standards.

- **Fabric & TurboModules:** Preparing the app for the New Architecture to benefit from direct C++ bindings.
- **Performance:** Eliminating the legacy bridge bottleneck to ensure smoother UI interactions on mid-range devices.

### 3. Pragmatic State Management (Recoil)

Instead of adopting a heavy boilerplate solution like Redux, I chose **Recoil** for atomic state management.

- **Reasoning:** For an application of this scope, Redux introduces unnecessary complexity.
- **Benefit:** Recoil offers a minimal, atomic API that allows for rapid development. This aligns with the principle of **"Right-Sizing the Architecture"**—avoiding over-engineering where a simpler solution suffices.

### 4. UI Strategy: Radical Simplicity

I consciously prioritized **Accessibility over Aesthetics**.

- **The Goal:** Zero-friction usage for users across all age groups.
- **The Execution:** Leveraged **NativeWind** to build a high-contrast, linear interface that minimizes cognitive load and maximizes render performance.

---

### 🏗️ Architecture Diagram

_(Please refer to the diagram below for the data flow)_

![Place your Architecture Diagram Here](assets/diagram.png)

> **Engineering Decision:**
> I implemented a relational database structure for the **Category System** to ensure referential integrity. When a user views a summary, the app performs efficient aggregation queries directly on the local database rather than processing arrays in memory, ensuring performance remains O(1) even as transaction history grows to thousands of records.

---

## 📷 Screenshots

|            Dashboard            |         Add Transaction         |       Category Management       |
| :-----------------------------: | :-----------------------------: | :-----------------------------: |
| ![Screen 1](assets/screen1.png) | ![Screen 2](assets/screen2.png) | ![Screen 3](assets/screen3.png) |

---

## 🔒 Proprietary Notice

**This is a closed-source commercial project.**

Due to the proprietary nature of the application (currently live on Google Play Store), the full source code is not publicly available in this repository.

However, I am available to provide a **live code walkthrough** or discuss specific implementation details (such as the Database Schema or Sync Logic) during the technical interview.

---

_Developed by **Barqi Fuady** - Senior Software Engineer_
