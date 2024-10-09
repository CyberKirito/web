<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HEHEHE</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
        }
        .container {
            text-align: center;
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        button {
            margin: 10px;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
        }
        #message {
            font-size: 18px;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Apakah kita jadi ke pantai?</h1>
        <button id="yesBtn">Ya</button>
        <button id="noBtn">Tidak</button>
        <p id="message"></p>
    </div>

    <script>
        const yesBtn = document.getElementById('yesBtn');
        const noBtn = document.getElementById('noBtn');
        const message = document.getElementById('message');

        yesBtn.addEventListener('click', () => {
            message.textContent = 'Yeay! Aku senang sekali. Kita bisa berangkat sabtu besok:)';
            yesBtn.style.display = 'none';
            noBtn.style.display = 'none';
        });

        noBtn.addEventListener('mouseover', () => {
            const maxX = window.innerWidth - noBtn.offsetWidth;
            const maxY = window.innerHeight - noBtn.offsetHeight;
            noBtn.style.position = 'absolute';
            noBtn.style.left = Math.floor(Math.random() * maxX) + 'px';
            noBtn.style.top = Math.floor(Math.random() * maxY) + 'px';
        });
    </script>
</body>
</html>
