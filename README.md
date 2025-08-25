<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Umar's Awesome Website</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Comic Sans MS', cursive, sans-serif; 
        }
        
        body {
            background: linear-gradient(135deg, #a1c4fd 0%, #c2e9fb 100%);
            min-height: 100vh;
            padding: 20px;
            color: #333;
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.9);
            border-radius: 20px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            position: relative;
            overflow: hidden;
        }
        
        .container::before {
            content: "";
            position: absolute;
            top: -50px;
            right: -50px;
            width: 200px;
            height: 200px;
            background: linear-gradient(45deg, #ff9a9e 0%, #fad0c4 100%);
            border-radius: 50%;
            z-index: -1;
            opacity: 0.7;
        }
        
        .container::after {
            content: "";
            position: absolute;
            bottom: -70px;
            left: -70px;
            width: 250px;
            height: 250px;
            background: linear-gradient(45deg, #84fab0 0%, #8fd3f4 100%);
            border-radius: 50%;
            z-index: -1;
            opacity: 0.7;
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
        }
        
        h1 {
            font-size: 3.5rem;
            color: #1a73e8;
            margin-bottom: 10px;
            text-shadow: 2px 2px 0px rgba(255, 255, 255, 0.8);
        }
        
        .subtitle {
            font-size: 1.8rem;
            color: #5f6368;
            margin-bottom: 20px;
        }
        
        .profile-card {
            background: white;
            border-radius: 15px;
            padding: 25px;
            margin-bottom: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            border-left: 8px solid #1a73e8;
        }
        
        .profile-item {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
            font-size: 1.4rem;
        }
        
        .profile-item:last-child {
            margin-bottom: 0;
        }
        
        .profile-item .emoji {
            font-size: 2rem;
            margin-right: 15px;
        }
        
        .profile-item .label {
            font-weight: bold;
            color: #1a73e8;
            margin-right: 10px;
            min-width: 150px;
        }
        
        .fun-section {
            background: linear-gradient(135deg, #ffecd2 0%, #fcb69f 100%);
            border-radius: 15px;
            padding: 25px;
            margin-bottom: 30px;
            text-align: center;
        }
        
        .fun-section h2 {
            font-size: 2.2rem;
            color: #e67e22;
            margin-bottom: 20px;
        }
        
        .mango-container {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin: 20px 0;
        }
        
        .mango {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, #f9d423 0%, #ff4e50 100%);
            border-radius: 50% 50% 50% 0;
            transform: rotate(-45deg);
            position: relative;
            cursor: pointer;
            transition: transform 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .mango:hover {
            transform: rotate(-45deg) scale(1.1);
        }
        
        .mango::before {
            content: "🥭";
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(45deg);
            font-size: 2.5rem;
        }
        
        .coding-section {
            background: linear-gradient(135deg, #d4fc79 0%, #96e6a1 100%);
            border-radius: 15px;
            padding: 25px;
            margin-bottom: 30px;
        }
        
        .coding-section h2 {
            font-size: 2.2rem;
            color: #2e7d32;
            margin-bottom: 20px;
            text-align: center;
        }
        
        .code-block {
            background: #263238;
            color: #eeffff;
            border-radius: 10px;
            padding: 20px;
            font-family: 'Courier New', monospace;
            font-size: 1.2rem;
            line-height: 1.6;
            overflow-x: auto;
            margin: 20px 0;
        }
        
        .code-block .keyword {
            color: #c792ea;
        }
        
        .code-block .string {
            color: #c3e88d;
        }
        
        .code-block .comment {
            color: #546e7a;
            font-style: italic;
        }
        
        .color-picker {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 15px;
            margin: 20px 0;
        }
        
        .color-option {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            cursor: pointer;
            transition: transform 0.3s ease;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        
        .color-option:hover {
            transform: scale(1.1);
        }
        
        .color-option.blue {
            background: #1a73e8;
        }
        
        .color-option.red {
            background: #ea4335;
        }
        
        .color-option.yellow {
            background: #fbbc05;
        }
        
        .color-option.green {
            background: #34a853;
        }
        
        .color-option.purple {
            background: #9c27b0;
        }
        
        .message {
            text-align: center;
            font-size: 1.8rem;
            color: #1a73e8;
            margin: 20px 0;
            padding: 15px;
            background: rgba(255, 255, 255, 0.7);
            border-radius: 10px;
        }
        
        footer {
            text-align: center;
            margin-top: 30px;
            padding: 20px;
            color: #5f6368;
            font-size: 1.2rem;
        }
        
        .footer-heart {
            color: #ea4335;
        }
        
        @media (max-width: 600px) {
            h1 {
                font-size: 2.8rem;
            }
            
            .subtitle {
                font-size: 1.5rem;
            }
            
            .profile-item {
                font-size: 1.2rem;
            }
            
            .mango {
                width: 60px;
                height: 60px;
            }
            
            .mango::before {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Umar's Awesome Website</h1>
            <div class="subtitle">🌟 Future Developer 🌟</div>
        </header>
        
        <section class="profile-card">
            <div class="profile-item">
                <span class="emoji">👦</span>
                <span class="label">Name:</span>
                <span>Umar</span>
            </div>
            <div class="profile-item">
                <span class="emoji">🎂</span>
                <span class="label">Age:</span>
                <span>8 years old</span>
            </div>
            <div class="profile-item">
                <span class="emoji">🎨</span>
                <span class="label">Favorite Color:</span>
                <span>Blue 💙</span>
            </div>
            <div class="profile-item">
                <span class="emoji">🥭</span>
                <span class="label">Favorite Fruit:</span>
                <span>Mango</span>
            </div>
            <div class="profile-item">
                <span class="emoji">💻</span>
                <span class="label">Learning:</span>
                <span>To be a Developer</span>
            </div>
            <div class="profile-item">
                <span class="emoji">✨</span>
                <span class="label">Loves:</span>
                <span>Coding, colors, and yummy mangoes!</span>
            </div>
        </section>
        
        <section class="fun-section">
            <h2>🥭 Umar's Mango Collection 🥭</h2>
            <p>Click on the mangoes to see them dance!</p>
            <div class="mango-container">
                <div class="mango" onclick="animateMango(this)"></div>
                <div class="mango" onclick="animateMango(this)"></div>
                <div class="mango" onclick="animateMango(this)"></div>
                <div class="mango" onclick="animateMango(this)"></div>
                <div class="mango" onclick="animateMango(this)"></div>
            </div>
        </section>
        
        <section class="coding-section">
            <h2>💻 Umar's First Code 💻</h2>
            <div class="code-block">
                <span class="comment">// Umar's first Python program</span><br>
                <span class="keyword">print</span>(<span class="string">"Hello, I'm Umar!"</span>)<br>
                <span class="keyword">print</span>(<span class="string">"I love coding and mangoes!"</span>)<br>
                <span class="keyword">print</span>(<span class="string">"Blue is my favorite color!"</span>)<br>
                <span class="comment"># I'm going to be a great developer!</span>
            </div>
            
            <h2 style="margin-top: 30px;">🎨 Umar's Color Picker 🎨</h2>
            <p>Click on a color to change the website theme!</p>
            <div class="color-picker">
                <div class="color-option blue" onclick="changeTheme('blue')"></div>
                <div class="color-option red" onclick="changeTheme('red')"></div>
                <div class="color-option yellow" onclick="changeTheme('yellow')"></div>
                <div class="color-option green" onclick="changeTheme('green')"></div>
                <div class="color-option purple" onclick="changeTheme('purple')"></div>
            </div>
        </section>
        
        <div class="message" id="message">
            Welcome to Umar's website! He's learning to code and loves mangoes! 🥭💻✨
        </div>
        
        <footer>
            Made with <span class="footer-heart">❤️</span> for Umar, the future developer!
        </footer>
    </div>

    <script>
        function animateMango(mango) {
            mango.style.transform = "rotate(-45deg) scale(1.2)";
            
            setTimeout(() => {
                mango.style.transform = "rotate(-45deg) scale(1)";
            }, 300);
            
            // Show a message
            const messages = [
                "Yummy mango! 🥭",
                "I love mangoes! 💛",
                "Mangoes are the best! 🌟",
                "Delicious! 😋",
                "Mango power! 💪"
            ];
            
            const randomMessage = messages[Math.floor(Math.random() * messages.length)];
            document.getElementById("message").textContent = randomMessage;
        }
        
        function changeTheme(color) {
            const body = document.body;
            const message = document.getElementById("message");
            
            switch(color) {
                case 'blue':
                    body.style.background = "linear-gradient(135deg, #a1c4fd 0%, #c2e9fb 100%)";
                    message.textContent = "Blue is Umar's favorite color! 💙";
                    break;
                case 'red':
                    body.style.background = "linear-gradient(135deg, #ff9a9e 0%, #fad0c4 100%)";
                    message.textContent = "Red is a vibrant color! 🔴";
                    break;
                case 'yellow':
                    body.style.background = "linear-gradient(135deg, #ffecd2 0%, #fcb69f 100%)";
                    message.textContent = "Yellow like mangoes! 🥭";
                    break;
                case 'green':
                    body.style.background = "linear-gradient(135deg, #84fab0 0%, #8fd3f4 100%)";
                    message.textContent = "Green like nature! 🌿";
                    break;
                case 'purple':
                    body.style.background = "linear-gradient(135deg, #d9a7c7 0%, #fffcdc 100%)";
                    message.textContent = "Purple is magical! ✨";
                    break;
            }
        }
    </script>
</body>
</html>
