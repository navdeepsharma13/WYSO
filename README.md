<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>WYSO - Professional Services</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap');
        :root {
            --primary-color: #0077cc;
            --secondary-color: #003d66;
            --background-color: #f9fbfd;
            --card-bg: #ffffff;
            --border-color: #d1d9e6;
            --text-color: #2a3a4a;
        }

        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            font-family: 'Inter', sans-serif;
            background-color: var(--background-color);
            color: var(--text-color);
            display: flex;
            flex-direction: column;
            min-height: 100vh;
        }

        header {
            background-color: var(--primary-color);
            color: white;
            padding: 20px;
            text-align: center;
            font-size: 2rem;
            font-weight: 700;
        }

        nav {
            display: flex;
            background: var(--background-color);
            border-bottom: 1px solid var(--border-color);
        }

        nav button {
            flex: 1;
            padding: 14px 0;
            font-weight: 600;
            font-size: 1rem;
            color: var(--secondary-color);
            border: none;
            background: none;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        nav button:hover,
        nav button.active {
            background-color: #e6f0ff;
            color: var(--primary-color);
        }

        main {
            flex: 1;
            padding: 20px;
            overflow-y: auto;
        }

        section {
            display: none;
            margin-top: 20px;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            background: var(--card-bg);
        }

        section.active {
            display: block;
        }

        h2 {
            color: var(--primary-color);
            margin-bottom: 10px;
        }

        /* Feedback Section styles */
        .feedback-container {
            margin-top: 20px;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            background: var(--card-bg);
            transition: background-color 0.3s ease, box-shadow 0.3s ease;
        }

        .feedback-container:hover {
            background-color: #f0f4ff; /* Light blue background on hover */
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
        }

        .contact-form label {
            margin-bottom: 5px;
            color: var(--primary-color);
        }

        .contact-form input,
        .contact-form textarea {
            margin-bottom: 10px;
            padding: 10px;
            border: 1px solid var(--border-color);
            border-radius: 4px;
            transition: border-color 0.3s ease;
        }

        .contact-form input:focus,
        .contact-form textarea:focus {
            border-color: var(--primary-color);
            outline: none;
        }

        .contact-form button {
            padding: 10px;
            background-color: var(--primary-color);
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        .contact-form button:hover {
            background-color: #005fa3; /* Darker shade on hover */
        }

        /* Chatbot styles */
        .chat-container {
            margin-top: 20px;
            border: 1px solid var(--border-color);
            border-radius: 8px;
            padding: 10px;
        }

        .chat-header {
            background-color: var(--primary-color);
            color: white;
            padding: 10px;
            text-align: center;
            border-radius: 8px 8px 0 0;
        }

        .chat-input {
            display: flex;
            margin-top: 10px;
        }

        .chat-input input {
            flex: 1;
            padding: 10px;
            border: 1px solid var(--border-color);
            border-radius: 4px;
        }

        .chat-input button {
            padding: 10px;
            background-color: var(--primary-color);
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            margin-left: 10px;
        }

        .chat-input button:hover {
            background-color: #005fa3;
        }

        /* Help Section styles */
        .faq-item {
            margin-bottom: 10px;
        }

        .faq-question {
            cursor: pointer;
            padding: 10px;
            background: var(--primary-color);
            color: white;
            border-radius: 4px;
        }

        .faq-answer {
            display: none;
            padding: 10px;
            border: 1px solid var(--border-color);
            border-radius: 4px;
            margin-top: 5px;
        }

        .faq-item.active .faq-answer {
            display: block;
        }

        /* Contact Form styles */
        .contact-form {
            display: flex;
            flex-direction: column;
        }

        /* Responsive styles */
        @media (max-width: 600px) {
            nav {
                flex-direction: column;
            }

            nav button {
                margin-bottom: 10px;
            }
        }
    </style>
</head>
<body>
    <header>
        WYSO - Professional Services
    </header>
    <nav>
        <button class="active" type="button" data-tab="home" aria-controls="home"><a href="home2.html">Home</button></a>
        <button type="button" data-tab="chat" aria-controls="chat"><a href="htmlip.html">Chatbot</button></a>
        <button type="button" data-tab="help" aria-controls="help"><a href="ip3.html">Help</button></a>
        <button type="button" data-tab="about" aria-controls="about"><a href="abou us.html">About Us</button></a>
        <button type="button" data-tab="feedback" aria-controls="feedback"><a href="feedback.html">Feedback</button></a>
    </nav>
    <main>
        <!-- Home Section -->
        <section id="home" class="active">
            <h2>Welcome to WYSO</h2>
            <p>Your one-stop solution for professional services. We are dedicated to providing top-notch services tailored to your needs.</p>
              <p>Today is <span id="current-date"></span>. Our chatbot is here to assist you with:</p>
            <ul>
                <li>General health inquiries</li>
                <li>Appointment scheduling</li>
                <li>Medication information</li>
                <li>Symptom checking</li>
                <li>Health tips and advice</li>
            </ul>
            <p>Feel free to ask any questions or type your message below to get started!</p>
        </section>

        <!-- Chatbot Section -->
        <section id="chat" hidden>
            <div class="chat-container">
                <div class="chat-header">
                    <h1>WYSO ChatBot</h1>
                </div>
                <div class="chat-messages" id="chat-messages">
                    <!-- Messages will be added here -->
                </div>
                <div class="chat-input">
                    <input type="text" id="user-input" placeholder="Type your message here...">
                    <button id="send-button">Send</button>
                </div>
            </div>
        </section>

        <!-- Help Section -->
        <section id="help" hidden>
            <h2>Help Center</h2>
            <!-- Help content... -->
        </section>

        <!-- About Us Section -->
        <section id="about" hidden>
            <h2>About Us</h2>
            <!-- About Us content... -->
        </section>

        <!-- Feedback Section -->
        <section id="feedback" hidden>
            <h2>Feedback</h2>
            <div class="feedback-container">
                <form class="contact-form" id="feedbackForm" novalidate>
                    <label for="feedback-name">Name*</label>
                    <input type="text" id="feedback-name" name="feedback-name" required aria-required="true" placeholder="Your name" />

                    <label for="feedback-email">Email*</label>
                    <input type="email" id="feedback-email" name="feedback-email" required aria-required="true" placeholder="you@example.com" />

                    <label for="feedback-message">Feedback*</label>
                    <textarea id="feedback-message" name="feedback-message" rows="5" required aria-required="true" placeholder="Your feedback here"></textarea>

                    <button type="submit">Submit Feedback</button>
                </form>
            </div>
        </section>
    </main>

    <script>
        // Tab Navigation
        const navButtons = document.querySelectorAll('nav button[data-tab]');
        const sections = document.querySelectorAll('main > section');

        navButtons.forEach(button => {
            button.addEventListener('click', () => {
                navButtons.forEach(btn => {
                    btn.classList.remove('active');
                });
                button.classList.add('active');

                const tabName = button.getAttribute('data-tab');
                sections.forEach(section => {
                    section.hidden = true;
                    if (section.id === tabName) {
                        section.hidden = false;
                    }
                });
            });
        });

        // Chatbot functionality (placeholder)
        document.getElementById('send-button').addEventListener('click', () => {
            const userInput = document.getElementById('user-input').value;
            const chatMessages = document.getElementById('chat-messages');
            const newMessage = document.createElement('div');
            newMessage.textContent = userInput;
            chatMessages.appendChild(newMessage);
            document.getElementById('user-input').value = '';
        });
    </script>
</body>
</html>
