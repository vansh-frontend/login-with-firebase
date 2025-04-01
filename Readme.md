<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Firebase Authentication - README</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
            padding: 20px;
            background-color: #f4f4f4;
        }
        h1, h2, h3 {
            color: #333;
        }
        pre {
            background: #333;
            color: #fff;
            padding: 10px;
            overflow-x: auto;
        }
        code {
            font-family: monospace;
        }
        img {
            max-width: 100%;
            height: auto;
        }
    </style>
</head>
<body>
    <h1>🔥 Firebase Authentication - Login & Signup</h1>
    <p>Welcome to the <strong>Firebase Authentication</strong> project! This repository provides a simple and efficient way to integrate <strong>Login and Signup</strong> functionality using Firebase with <strong>HTML, CSS, and JavaScript</strong>.</p>
    
    <h2>🚀 Features</h2>
    <ul>
        <li>✅ User <strong>Signup</strong> with Email & Password</li>
        <li>✅ User <strong>Login</strong> with Email & Password</li>
        <li>✅ Firebase <strong>Authentication</strong> Integration</li>
        <li>✅ Secure <strong>Firestore Database</strong> for storing user data</li>
        <li>✅ <strong>Responsive UI</strong> built with HTML, CSS, and JavaScript</li>
    </ul>
    
    <h2>🎯 Preview</h2>
    <img src="img/login.png" alt="Login Screen">
    <img src="img/signup.png" alt="Signup Screen">
    
    
    <h2>📂 Project Structure</h2>
    <pre>
📦 firebase-auth-app
 ┣ 📂 assets
 ┃ ┣ 📜 styles.css
 ┃ ┗ 📜 script.js
 ┣ 📜 index.html
 ┣ 📜 login.html
 ┣ 📜 signup.html
 ┣ 📜 firebase-config.js
 ┣ 📜 README.md
 ┗ 📜 .gitignore
    </pre>
    
    <h2>🔧 Installation & Setup</h2>
    <h3>1️⃣ Clone the Repository</h3>
    <pre><code>git clone https://github.com/vansh-frontend/login-with-firebase
cd firebase-auth-app</code></pre>
    
    <h3>2️⃣ Setup Firebase</h3>
    <p>1. Go to <a href="https://console.firebase.google.com/">Firebase Console</a></p>
    <p>2. Create a new Firebase project</p>
    <p>3. Enable <strong>Authentication</strong> (Email & Password)</p>
    <p>4. Create a Firestore Database (if needed)</p>
    <p>5. Copy your Firebase configuration and paste it into <code>firebase-config.js</code></p>
    
    <pre><code>// firebase-config.js
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_STORAGE_BUCKET",
  messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
  appId: "YOUR_APP_ID"
};

firebase.initializeApp(firebaseConfig);
const auth = firebase.auth();</code></pre>
    
    <h2>🔑 User Authentication Flow</h2>
    <ul>
        <li>1️⃣ <strong>Signup Page</strong>: Users can create an account with Email & Password.</li>
        <li>2️⃣ <strong>Login Page</strong>: Users can log in with their credentials.</li>
        <li>3️⃣ <strong>Dashboard</strong>: Users can access a protected page after authentication.</li>
    </ul>
    
    <h2>📜 Code Examples</h2>
    
    <h3>📌 Signup Functionality</h3>
    <pre><code>// script.js
function signUp() {
    var email = document.getElementById("email").value;
    var password = document.getElementById("password").value;
    
    auth.createUserWithEmailAndPassword(email, password)
        .then((userCredential) => {
            alert("Signup Successful");
        })
        .catch((error) => {
            alert(error.message);
        });
}</code></pre>
    
    <h3>📌 Login Functionality</h3>
    <pre><code>function login() {
    var email = document.getElementById("email").value;
    var password = document.getElementById("password").value;
    
    auth.signInWithEmailAndPassword(email, password)
        .then((userCredential) => {
            alert("Login Successful");
            window.location.href = "dashboard.html";
        })
        .catch((error) => {
            alert(error.message);
        });
}</code></pre>
    
    <h2>🌟 Contributing</h2>
    <p>We welcome contributions! Feel free to <strong>fork</strong> this repo, create a new branch, and submit a pull request.</p>
    
    <h2>📜 License</h2>
    <p>This project is licensed under the <strong>MIT License</strong>.</p>
    
    <h2>📞 Contact</h2>
    <p>For any queries, reach out to <strong>[Your Name]</strong> at <strong>your-email@example.com</strong></p>
</body>
</html>