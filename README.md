✨ AI-Powered My Task Tracker 🚀

A modern, real-time, and collaborative Kanban board application supercharged with AI features. This tool helps you manage your workflow seamlessly with an intuitive drag-and-drop interface, while leveraging the power of Google's Gemini AI to automate and enhance task creation.

Live Demo: [file:///C:/Users/laptop/Desktop/my-task-tracker/index.html] 


🌟 Features
Kanban Board: A classic three-column layout ("To Do", "In Progress", "Done") to visualize your workflow.

Real-time Collaboration: Powered by Firebase Firestore, all changes are synced instantly across all users viewing the board.

Drag & Drop: Intuitively move tasks between columns to update their status.

CRUD Functionality: Easily Create, Read, Update, and Delete tasks.

🎉 Confetti Celebration: A fun confetti animation triggers every time a task is moved to the "Done" column.

🤖 AI-Powered Features (via Gemini AI):

Generate Task Description: Automatically generate a detailed task description from just a title.

Suggest Sub-tasks: Break down a complex task into smaller, actionable sub-tasks, which are automatically added to your "To Do" list.

Secure Anonymous Authentication: Each user is given a unique anonymous identity using Firebase Authentication.

🛠️ Tech Stack
Frontend: HTML5, JavaScript (ES6 Modules)

Styling: Tailwind CSS

Backend & Database: Google Firebase (Firestore, Authentication)

AI: Google Gemini API

Animations: canvas-confetti

📋 Prerequisites
Before you begin, ensure you have the following:

A Google Account.

A code editor (like VS Code).

A modern web browser (like Chrome, Firefox).

🚀 Setup and Installation Guide
To get a local copy up and running, follow these simple steps.

Step 1: Clone the Repository
First, clone this repository to your local machine.

Bash

git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
Step 2: Set up Firebase
This project uses Firebase for its database and authentication. You need to create your own Firebase project.

Create a Firebase Project:

Go to the Firebase Console.

Click on "+ Add project" and give it a name (e.g., "My Kanban App").

Follow the on-screen steps to create the project.

Enable Authentication:

In your project's dashboard, go to Build > Authentication.

Click the "Get started" button.

In the "Sign-in method" tab, select "Anonymous" from the list, enable it, and click "Save".

Set up Firestore Database:

From the side menu, go to Build > Firestore Database.

Click "Create database".

Choose to start in Test mode (this allows easy read/write access for the next 30 days).

Select a location for your database and click "Enable".

Get Firebase Configuration:

In your project dashboard, click the gear icon (⚙️) > Project settings.

In the "General" tab, scroll down to the "Your apps" section.

Click the web icon </> to create a new web app.

Give it a nickname and click "Register app".

Firebase will provide you with a firebaseConfig object. Copy this object.

Step 3: Get Your Gemini API Key
Go to Google AI Studio.

Log in with your Google account.

Click on "Get API key" > "Create API key".

Copy the generated API key.

Step 4: Configure the Application
Now, you need to add the keys you just created into the index.html file.

Open the index.html file in your code editor.

Find the <script type="module"> section at the bottom.

Update Firebase Config: Find the line const firebaseConfig = ... and replace the placeholder object with the firebaseConfig you copied from Firebase.

JavaScript

// BEFORE
const firebaseConfig = typeof __firebase_config !== 'undefined' ? JSON.parse(__firebase_config) : {};

// AFTER (Paste your config here)
const firebaseConfig = {
  apiKey: "AIza...",
  authDomain: "your-project-id.firebaseapp.com",
  projectId: "your-project-id",
  storageBucket: "your-project-id.appspot.com",
  messagingSenderId: "1234567890",
  appId: "",
  measurementId: ""
};
Update Gemini API Key: Find the line const apiKey = ""; and paste your Gemini API key inside the quotes.

JavaScript

// BEFORE
const apiKey = ""; 

// AFTER
const apiKey = "YOUR_GEMINI_API_KEY_HERE";
Save the index.html file.

Step 5: Run the Application
You're all set! To run the app, simply open the index.html file in your web browser.

Navigate to the project directory on your computer.

Double-click the index.html file.

The Kanban board should now be fully functional, connected to your Firebase backend and Gemini AI.

🌐 Deployment (Optional)
You can easily deploy this application for free using GitHub Pages.

Push your code with the updated configuration to your GitHub repository.

In your repository, go to Settings > Pages.

Under the "Branch" section, select the main (or master) branch and click "Save".

GitHub will generate a public URL for your live application. It may take a few minutes to go live.
