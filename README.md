# mood-based-quote-project
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mood-Based Quote Generator</title>
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #ff9a9e, #fad0c4);
            text-align: center;
            padding: 20px;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }
        h1 {
            color: #fff;
            font-size: 28px;
            margin-bottom: 20px;
        }
        .mood-buttons {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin: 20px 0;
        }
        button {
            padding: 12px 24px;
            border: none;
            background: #ff6f91;
            color: white;
            font-size: 18px;
            border-radius: 25px;
            cursor: pointer;
            transition: 0.3s;
            display: flex;
            align-items: center;
            gap: 8px;
            box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
        }
        button:hover {
            background: #ff3e68;
            transform: scale(1.05);
        }
        #quote {
            font-size: 22px;
            color: #fff;
            margin-top: 20px;
            padding: 15px;
            background: rgba(255, 255, 255, 0.2);
            display: inline-block;
            border-radius: 12px;
            max-width: 80%;
            font-style: italic;
            box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
        }
    </style>
</head>
<body>
    <h1>How are you feeling today? 😊</h1>
    <div class="mood-buttons">
        <button onclick="generateQuote('happy')">😊 Happy</button>
        <button onclick="generateQuote('calm')">🌿 Calm</button>
        <button onclick="generateQuote('inspired')">💡 Inspired</button>
        <button onclick="generateQuote('motivated')">🔥 Motivated</button>
    </div>
    <p id="quote">Click a mood to get a quote! ✨</p>
    
    <script>
        const quotes = {
            happy: [
                "Happiness is not by chance, but by choice. 😊",
                "The best way to cheer yourself is to try to cheer someone else up. 🎈",
                "Happiness is contagious—spread it! ✨"
            ],
            calm: [
                "Breathe in, breathe out, and let it all go. 🌿",
                "Calm mind brings inner strength and self-confidence. 🌸",
                "Peace comes from within. Do not seek it without. ☮️"
            ],
            inspired: [
                "Believe in yourself and all that you are. 💡",
                "Dream big and dare to fail. 🚀",
                "The best way to predict the future is to create it. 🎯"
            ],
            motivated: [
                "Push yourself, because no one else is going to do it for you. 🔥",
                "Don't stop when you're tired. Stop when you're done. 💪",
                "Success is not for the lazy. Keep pushing forward! 🚀"
            ]
        };

        function generateQuote(mood) {
            const randomIndex = Math.floor(Math.random() * quotes[mood].length);
            document.getElementById('quote').textContent = quotes[mood][randomIndex];
        }
    </script>
</body>
</html>

