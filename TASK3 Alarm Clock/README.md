# Alarm Clock App

<img src="path_to_your_logo_image.png" alt="Logo" width="150" height="150">

The Alarm Clock App is designed to help users set and manage alarms with ease. This app features an intuitive interface and includes all the functionalities needed for effective alarm management.

## Table of Contents

- [Features](#features)
- [Screenshots](#screenshots)
- [Installation](#installation)
- [Firebase Setup](#firebase-setup)
- [Usage](#usage)
- [Contributing](#contributing)
- [Contact](#contact)
- [Demo](#demo)

## Features

- **Home Screen**: Display current time and date.
- **Alarm Setting**: Time picker to set the alarm time.
- **Option to Choose Alarm Tone**: Allow users to select the alarm tone.
- **Alarm Management**: List of all set alarms with on/off toggle.
- **Snooze and Dismiss**: Snooze or dismiss the alarm when it rings.
- **User Interface**: User-friendly and visually appealing design.

## Screenshots

Include some screenshots of your app to give users a visual idea of what your app looks like.

![Screenshot1](link_to_screenshot1)
![Screenshot2](link_to_screenshot2)
![Screenshot3](link_to_screenshot3)

## Installation

### Prerequisites

- Android Studio installed on your machine
- A device or emulator to run the app

### Steps

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/alarm-clock-app.git
    ```
2. Open the project in Android Studio.
3. Let Android Studio install any required dependencies.
4. Build and run the app on your device or emulator.

## Firebase Setup

1. Go to the [Firebase Console](https://console.firebase.google.com/) and create a new project.
2. In your Firebase project, add an Android app and follow the setup steps. You'll need the package name of your Android app.
3. Download the `google-services.json` file provided by Firebase and place it in your project's `app` directory.
4. Add the Firebase SDK to your project. Update your `build.gradle` files as follows:

**Project-level `build.gradle` (`build.gradle`)**:
    ```gradle
    buildscript {
        dependencies {
            classpath 'com.google.gms:google-services:4.3.10'  // Check for the latest version
        }
    }
    ```

**App-level `build.gradle` (`app/build.gradle`)**:
    ```gradle
    apply plugin: 'com.android.application'
    apply plugin: 'com.google.gms.google-services'

    dependencies {
        // Firebase SDK
        implementation platform('com.google.firebase:firebase-bom:31.1.1') // Check for the latest version
        implementation 'com.google.firebase:firebase-storage'
        implementation 'com.google.firebase:firebase-auth'
        implementation 'com.google.firebase:firebase-database'
        // Other dependencies
    }
    ```

5. Initialize Firebase in your application. Update your `MainActivity.java` or `MainActivity.kt`:
    ```java
    import com.google.firebase.FirebaseApp;

    @Override
    public void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        FirebaseApp.initializeApp(this);
        // Other initialization code
    }
    ```

## Usage

1. Open the app to view the current time and date.
2. Tap the "Add Alarm" button to set a new alarm.
3. Use the time picker to choose the alarm time.
4. Select the alarm tone from the available options.
5. Save the alarm to see it listed on the home screen.
6. Toggle alarms on or off as needed.
7. When an alarm rings, choose to snooze or dismiss it.

## Contributing

Contributions are welcome! If you'd like to contribute, please fork the repository and use a feature branch. Pull requests are warmly welcomed.

1. Fork the repository.
2. Create a new branch:
    ```bash
    git checkout -b feature/YourFeature
    ```
3. Make your changes.
4. Commit your changes:
    ```bash
    git commit -m 'Add some feature'
    ```
5. Push to the branch:
    ```bash
    git push origin feature/YourFeature
    ```
6. Create a new pull request.

## Contact

Your Name - [your.email@example.com](mailto:your.email@example.com)

Project Link: [https://github.com/yourusername/alarm-clock-app](https://github.com/yourusername/alarm-clock-app)

## Demo

Check out a video demo of the Alarm Clock App on YouTube: [Click here for demo](https://www.youtube.com/link_to_alarm_clock_demo)
