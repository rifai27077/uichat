<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Firestore Chat</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            padding: 20px;
        }

        form {
            margin-bottom: 20px;
        }

        input[type="submit"] {
            margin-left: 10px;
        }

        #messages {
            list-style-type: none;
            padding: 10px;
            margin: 0;
            max-height: 400px; /* Adjust as needed */
            overflow-y: auto;
            border: 1px solid #ccc;
            background: #f9f9f9;
            margin-top: 20px;
            border-radius: 5px;
        }

        #messages li {
            padding: 8px;
            border-bottom: 1px solid #ddd;
            margin-bottom: 5px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        #messages li button {
            background: #ff5c5c;
            border: none;
            color: white;
            padding: 3px 6px;
            border-radius: 3px;
            cursor: pointer;
        }

        #messages li button:hover {
            background: #ff3a3a;
        }
    </style>
    <script type="module">
        // Import the functions you need from the SDKs you need
        import { initializeApp } from "https://www.gstatic.com/firebasejs/10.13.1/firebase-app.js";
        import { getFirestore, collection, addDoc, onSnapshot, deleteDoc, doc } from "https://www.gstatic.com/firebasejs/10.13.1/firebase-firestore.js";
        
        // Your web app's Firebase configuration
        const firebaseConfig = {
            apiKey: "AIzaSyAVnc78CVeW18QI_8PGMoUxc8rQKuclaSM",
            authDomain: "socialmediaapp-33856.firebaseapp.com",
            projectId: "socialmediaapp-33856",
            storageBucket: "socialmediaapp-33856.appspot.com",
            messagingSenderId: "832803806835",
            appId: "1:832803806835:web:4f4c4d1739e0cee6281406",
            measurementId: "G-WSQL8E6VYG"
        };

        // Initialize Firebase
        const app = initializeApp(firebaseConfig);
        const db = getFirestore(app);
        const myName = prompt('Enter your name');

        // Function to delete a message
        window.deleteMessage = async (messageId) => {
            if (confirm('Are you sure you want to delete this message?')) {
                try {
                    await deleteDoc(doc(db, "messages", messageId));
                    console.log('Message deleted successfully');
                    alert("Message deleted successfully!");
                } catch (error) {
                    console.error("Error deleting document: ", error);
                }
            }
        };

        document.addEventListener('DOMContentLoaded', () => {
            const form = document.querySelector('form');
            form.addEventListener('submit', async (event) => {
                event.preventDefault();
                const message = document.getElementById('message').value;
                try {
                    await addDoc(collection(db, "messages"), {
                        sender: myName,
                        message: message
                    });
                    console.log('Message sent successfully');
                    alert("Message sent successfully!");
                    document.getElementById('message').value = ""; // Clear the input field
                } catch (error) {
                    console.error("Error adding document: ", error);
                }
            });

            // Listen for incoming messages
            const messagesRef = collection(db, "messages");
            onSnapshot(messagesRef, (snapshot) => {
                let html = "";
                snapshot.forEach(doc => {
                    const data = doc.data();
                    html += `<li>${data.sender}: ${data.message} <button onclick="deleteMessage('${doc.id}')">Delete</button></li>`;
                });
                const messagesList = document.getElementById('messages');
                messagesList.innerHTML = html;
                // Scroll to the bottom of the messages list
                messagesList.scrollTop = messagesList.scrollHeight;
            });
        });
    </script>
</head>
<body>
    <!-- create a form to send messages -->
    <form>
        <input id="message" placeholder="Enter message" autocomplete="off">
        <input type="submit" value="Send">
    </form>

    <!-- create a list -->
    <ul id="messages"></ul>
</body>
</html>
