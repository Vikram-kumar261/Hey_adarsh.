<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Vikram Kumar Azad | Study Hub</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Vikram Kumar Azad's Study Hub 📘</h1>
        <nav>
            <a href="#">Home</a>
            <a href="#">About</a>
            <a href="#">Study Materials</a>
            <a href="#">AI Assistant</a>
            <a href="#">Tools</a>
            <a href="#">Quiz</a>
            <a href="#">Contact</a>
        </nav>
    </header>

    <main>
        <section class="hero">
            <h2>Welcome Students 👋</h2>
            <p>Your one-stop solution for all study needs.</p>
            <button onclick="alert('AI Assistant will be added soon!')">Ask AI Doubts</button>
        </section>

        <section class="features">
            <div class="card">
                <h3>📚 Study Materials</h3>
                <p>Download notes, PDFs, and more.</p>
            </div>
            <div class="card">
                <h3>🧠 AI Assistant</h3>
                <p>Ask doubts and get instant answers.</p>
            </div>
            <div class="card">
                <h3>🧮 Tools</h3>
                <p>Calculator, Unit Converter and more.</p>
            </div>
            <div class="card">
                <h3>📝 Quiz</h3>
                <p>Test your knowledge with quizzes.</p>
            </div>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 Vikram Kumar Azad | All rights reserved.</p>
    </footer>
</body>
</html>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', sans-serif;
}

body {
    background: linear-gradient(to right, #f0f8ff, #e6f7ff);
    color: #333;
}

header {
    background-color: #004080;
    color: white;
    padding: 20px;
    text-align: center;
}

nav {
    margin-top: 10px;
}

nav a {
    color: #fff;
    margin: 0 15px;
    text-decoration: none;
    font-weight: bold;
}

.hero {
    text-align: center;
    padding: 60px 20px;
    background-color: #e0f7fa;
}

.hero h2 {
    font-size: 2.5rem;
    margin-bottom: 10px;
}

.hero button {
    margin-top: 20px;
    padding: 10px 20px;
    font-size: 1rem;
    background-color: #007acc;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

.features {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    padding: 40px 20px;
    background-color: #fff;
}

.card {
    background-color: #dff9fb;
    border: 2px solid #00a8ff;
    border-radius: 10px;
    width: 200px;
    padding: 20px;
    margin: 10px;
    text-align: center;
    transition: 0.3s;
}

.card:hover {
    transform: scale(1.05);
    background-color: #c7ecee;
}

footer {
    background-color: #004080;
    color: white;
    text-align: center;
    padding: 15px;
}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>AI Assistant | Vikram Kumar Azad</title>
    <link rel="stylesheet" href="style.css">
    <style>
        .chatbox {
            max-width: 600px;
            margin: 50px auto;
            background: #ffffff;
            border: 2px solid #007acc;
            border-radius: 10px;
            padding: 20px;
        }

        .messages {
            height: 300px;
            overflow-y: auto;
            border: 1px solid #ccc;
            padding: 10px;
            margin-bottom: 15px;
            background-color: #f9f9f9;
        }

        .message {
            margin-bottom: 10px;
        }

        .user {
            color: #007acc;
            font-weight: bold;
        }

        .bot {
            color: #28a745;
            font-weight: bold;
        }

        input[type="text"] {
            width: 80%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        button {
            padding: 10px 15px;
            background-color: #007acc;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        button:hover {
            background-color: #005f99;
        }
    </style>
</head>
<body>
    <header>
        <h1>AI Assistant 🤖</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="#">Study Materials</a>
            <a href="chatbot.html">AI Assistant</a>
            <a href="#">Tools</a>
            <a href="#">Contact</a>
        </nav>
    </header>

    <main>
        <div class="chatbox">
            <h2>Ask Your Doubts</h2>
            <div class="messages" id="chatMessages">
                <div class="message bot"><span class="bot">AI:</span> Hello! How can I help you today?</div>
            </div>
            <input type="text" id="userInput" placeholder="Type your question...">
            <button onclick="sendMessage()">Send</button>
        </div>
    </main>

    <footer>
        <p>&copy; 2025 Vikram Kumar Azad | All rights reserved.</p>
    </footer>

    <script>
        function sendMessage() {
            const input = document.getElementById('userInput');
            const message = input.value.trim();
            if (message === '') return;

            const chat = document.getElementById('chatMessages');
            const userMessage = `<div class="message user"><span class="user">You:</span> ${message}</div>`;
            chat.innerHTML += userMessage;

            // Dummy AI reply (You can replace this with real API later)
            const botReply = `<div class="message bot"><span class="bot">AI:</span> That's a great question! I'm still learning, but here's a suggestion: Keep studying and stay curious. 😊</div>`;
            setTimeout(() => {
                chat.innerHTML += botReply;
                chat.scrollTop = chat.scrollHeight;
            }, 500);

            input.value = '';
            chat.scrollTop = chat.scrollHeight;
        }
    </script>
</body>
</html>
