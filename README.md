<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For Varsha</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #fce4ec;
            font-family: 'Arial', sans-serif;
            margin: 0;
            overflow: hidden;
            flex-direction: column;
        }
        .container {
            text-align: center;
            background: white;
            padding: 50px;
            border-radius: 20px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
            position: relative;
            z-index: 1;
        }
        h1 { color: #d81b60; font-size: 2rem; }
        .buttons { margin-top: 30px; position: relative; height: 50px; }
        button {
            padding: 15px 30px;
            font-size: 18px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: 0.3s;
        }
        #yesBtn { background-color: #ff4081; color: white; margin-right: 10px; }
        #noBtn {
            background-color: #fb8c00;
            color: white;
            position: absolute;
        }
        .footer {
            margin-top: 50px;
            color: #880e4f;
            font-weight: bold;
            font-style: italic;
        }
        .cat-img { width: 100px; margin-bottom: 20px; }
    </style>
</head>
<body>

    <div class="container">
        <div class="cat-img">🐱💝</div>
        <h1 id="question">VARSHA will you be my valentine?</h1>
        <div class="buttons">
            <button id="yesBtn" onclick="celebrate()">Yes</button>
            <button id="noBtn" onmouseover="moveButton()">No</button>
        </div>
    </div>

    <div class="footer">
        Motu you don't have any option select Yes ~ Kevin
    </div>

    <script>
        function moveButton() {
            const noBtn = document.getElementById('noBtn');
            const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
            const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);
            
            noBtn.style.left = x + 'px';
            noBtn.style.top = y + 'px';
            noBtn.style.position = 'fixed';
        }

        function celebrate() {
            document.getElementById('question').innerHTML = "Yay! See you soon! ❤️";
            document.querySelector('.buttons').style.display = 'none';
            document.body.style.backgroundColor = "#ff80ab";
            alert("Good choice, Motu! 😉");
        }
    </script>
</body>
</html>
