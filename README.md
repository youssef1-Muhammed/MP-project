1. Project Overview
Laza is a Flutter-based e-commerce platform. It provides a seamless shopping experience including user authentication (Firebase), product categories, favorites, and a shopping cart.

2. How to Install Flutter & Project Dependencies
Download and install Flutter SDK from flutter.dev.

Clone this repository.

Open terminal in the project folder and run:

flutter pub get (to install all packages).

Connect an emulator or physical device.

Run the app using:

flutter run

3. Firebase Setup Steps
Create a project on Firebase Console.

Add an Android app with package name com.example.laza_ecommerce.

Download the google-services.json file.

Place the file in the android/app/ directory.

Enable 'Email/Password' in Firebase Authentication.

Create a Cloud Firestore database.

4. Firestore Rules Installation
Go to Firebase Console -> Firestore Database -> Rules tab.

Copy the content from the firestore.rules file in this repository.

Paste it into the console and click 'Publish'.

These rules ensure only authenticated users can access their own carts and favorites.

5. How to Run Android & iOS Builds
For Android:

Run flutter build apk --release to generate the APK file.

The file will be located at build/app/outputs/flutter-apk/app-release.apk.

For iOS:

(Requires macOS and Xcode)

Run flutter build ios

6. How to Run Appium Tests
Pre-conditions:

Appium Server must be running on http://127.0.0.1:4723.

Android device must be connected with USB Debugging enabled.

Python installed with Appium-Python-Client.

Execution:

Navigate to /appium_tests folder.

Run the command:

python auth_test.py

The script will automatically:

Perform Login.

Navigate to Home.

Add a product to the cart.

Verify the cart contents.
