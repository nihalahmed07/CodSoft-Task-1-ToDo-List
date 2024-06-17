# To-Do List App

<img src="app/src/main/ic_launcher-playstore.png" alt="Logo" width="150" height="150">

The To-Do List App is a simple yet powerful tool to help you manage your tasks efficiently. It allows users to add, edit, and delete tasks, as well as set priorities and due dates, and mark tasks as completed. Firebase Storage is used to store and retrieve tasks for data persistence.

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

- **Home Screen**: Display a list of tasks with titles and completion status.
- **Task Creation**: Allow users to add new tasks with titles and optional descriptions.
- **Task Editing**: Provide the ability to edit task titles and descriptions.
- **Task Completion**: Allow users to mark tasks as completed or active.
- **Task Deletion**: Add the option to delete tasks from the list.
- **Task Priorities**: Set priorities for tasks.
- **Due Dates**: Assign due dates to tasks.
- **User Login**: Users can access their todo list data from anywhere just by login their credentials .
- **Firebase Storage**: Store and retrieve tasks using Firebase Storage for data persistence across devices.
- **User Interface**: intuitive and user-friendly interface.

## Screenshots

Include some screenshots of your app to give users a visual idea of what your app looks like.

<img src="images/splash.jpg" alt="Main" width="290" height="550">
<img src="images/sign-in.jpg" alt="Sign-in" width="290" height="550">
<img src="images/sign-up.jpg" alt="Sign-up" width="290" height="550">
<img src="images/task.jpg" alt="Task" width="290" height="550">

## Installation

### Prerequisites

- Android Studio installed on your machine
- A device or emulator to run the app

### Steps

1. Clone the repository:
    ```bash
    git clone https://github.com/nihalahmed07/CodSoft-Task-1-ToDo-List.git
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

1. Open the app to view your list of tasks.
2. Tap the "Add Task" button to create a new task.
3. Fill in the task title and optional description, set priority and due date, then save.
4. Tap on a task to edit its details.
5. Swipe left or right on a task to mark it as completed or delete it.
6. All tasks are saved locally on your device and synced with Firebase Storage for persistence across devices.

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

Nihal Ahmed - [n.nihalahmed1@gmail.com](mailto:n.nihalahmed1@gmail.com)

Project Link: [To-Do List App](https://github.com/nihalahmed07/CodSoft-Task-1-ToDo-List)

## Demo

Check out a video demo of the application on YouTube: [Click here for demo](https://www.youtube.com/link_to_your_demo)
