# Firebase Lab (`firebaselab`)

An Android application built with Kotlin that demonstrates user authentication using **Firebase Authentication** (Email & Password login/registration flow).

---

## 📱 Features

- **User Registration (`RegistrationActivity`)**: 
  - Allows new users to create an account using an email address and password.
  - Form validation for empty fields and matching password/confirm password entries.
- **User Login (`LoginActivity`)**: 
  - Authenticates existing users with email and password via Firebase Auth.
- **Main View (`MainActivity`)**: 
  - Displays the authenticated user's email address upon successful login.
  - Supports signing out and navigating back to the login screen.
- **Graceful Configuration Handling**: 
  - Gracefully detects missing `google-services.json` / Firebase setup and alerts the user.

---

## 🛠️ Tech Stack & Requirements

- **Language:** Kotlin
- **Minimum SDK:** 31 (Android 12)
- **Target SDK:** 36
- **UI Framework:** Android XML Layouts, AppCompat, Material Components
- **Backend / Authentication:** Firebase Auth (`com.google.firebase:firebase-auth`)

---

## ⚙️ Setup & Installation

### 1. Prerequisites
- [Android Studio](https://developer.android.com/studio) (recent version)
- JDK 11 or higher

### 2. Clone the Repository
```bash
git clone <repository-url>
cd firebaselab
```

### 3. Firebase Configuration
To connect this project with your Firebase account:

1. Go to the [Firebase Console](https://console.firebase.google.com/).
2. Create a new Firebase project (or select an existing one).
3. Add an **Android app** to the Firebase project with the package name:
   `com.example.firebaselab`
4. Download the `google-services.json` file provided by Firebase.
5. Place `google-services.json` in the `app/` directory of this project:
   ```
   firebaselab/
   └── app/
       └── google-services.json
   ```
6. In the Firebase Console, navigate to **Authentication** > **Sign-in method** and enable **Email/Password**.
7. *(Optional)* Add the Google Services plugin in `build.gradle.kts` if connecting to live Firebase services:
   ```kotlin
   // In root build.gradle.kts:
   plugins {
       id("com.google.gms.google-services") version "4.4.2" apply false
   }
   
   // In app/build.gradle.kts:
   plugins {
       id("com.google.gms.google-services")
   }
   ```

---

## 🚀 Building & Running

1. Open the project in **Android Studio**.
2. Sync the project with Gradle files (**File > Sync Project with Gradle Files**).
3. Select an emulator or connected Android device running API 31+.
4. Click **Run** (`Shift + F10`) or deploy via Android Studio.

---

## 📄 License

This project is open-source and available for learning and experimentation purposes.

