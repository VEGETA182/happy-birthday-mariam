<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Mariam</title>
    <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Times+New+Roman&display=swap" rel="stylesheet">
    <style>
        body {
            margin: 0;
            font-family: 'Times New Roman', serif;
            background-color: #fce4ec;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            overflow: hidden;
        }

        #app {
            width: 100%;
            height: 100%;
            position: relative;
        }

        .slide {
            width: 100%;
            height: 100%;
            position: absolute;
            top: 0;
            left: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            background: url('birthday_background.jpg') no-repeat center center / cover;
            color: red;
            text-align: center;
            padding: 20px;
            transition: opacity 1s ease, transform 1s ease;
            opacity: 0;
            transform: scale(0.9);
            pointer-events: none;
        }

        .slide.visible {
            opacity: 1;
            transform: scale(1);
            pointer-events: auto;
        }

        .content {
            background: rgba(255, 255, 255, 0.9);
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
            max-width: 600px;
        }

        h1 {
            font-family: 'Times New Roman', serif;
            font-size: 3rem;
            margin-bottom: 10px;
            color: red;
        }

        p {
            font-size: 1.5rem;
            margin: 15px 0;
            color: red;
        }

        button {
            background-color: #ff6f61;
            color: #fff;
            border: none;
            padding: 15px 30px;
            font-size: 1.2rem;
            border-radius: 25px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        button:hover {
            background-color: #e0554d;
        }

        .balloons {
            font-size: 3rem;
        }

        .image {
            margin: 20px 0;
        }

        .image img {
            max-width: 100%;
            border-radius: 15px;
            box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
        }
    </style>
</head>
<body>
    <div id="app">
        <div class="slide visible" id="slide1">
            <div class="content">
                <h1 class="balloons">🎈🎈🎈 Hey Birthday Girl 🎈🎈🎈</h1>
                <p>Click Next to Proceed</p>
                <button onclick="nextSlide()">Next</button>
            </div>
        </div>
        <div class="slide" id="slide2">
            <div class="content">
                <p>Step 1: Wishing you a day filled with love and joy!</p>
                <div class="image">
                    <img src="WhatsApp Image 2025-02-09 at 04.48.47_993b18ee.jpg" alt="Childhood Memories">
                </div>
                <button onclick="nextSlide()">Next</button>
            </div>
        </div>
        <div class="slide" id="slide3">
            <div class="content">
                <p>Step 2: May all your dreams come true this year!</p>
                <div class="image">
                    <img src="WhatsApp Image 2025-02-06 at 01.54.45_71b4b920.jpg" alt="Recent Memories">
                </div>
                <button onclick="nextSlide()">Next</button>
            </div>
        </div>
        <div class="slide" id="slide4">
            <div class="content">
                <p>Step 3: Here’s to more laughs, love, and memories!</p>
                <button onclick="nextSlide()">Next</button>
            </div>
        </div>
        <div class="slide" id="slide5">
            <div class="content">
                <p>Step 4: You’re an amazing friend, and I’m so lucky to have you!</p>
                <button onclick="nextSlide()">Next</button>
            </div>
        </div>
        <div class="slide" id="slide6">
            <div class="content">
                <h1 class="balloons">🎈🎈🎈 Happy Birthday Mariam 🎈🎈🎈</h1>
                <p>Mariam, I honestly don’t know what I would do without you. You’ve been my light on the darkest days and my biggest cheerleader in every moment. Your kindness, your laughter, and your endless support have made my life so much brighter. I’m beyond grateful to have you as my best friend. You’re truly one of a kind, and I hope you always know how special you are to me. As a best friend, I love you for real.</p>
                <button onclick="restart()">Restart</button>
            </div>
        </div>
    </div>

    <script>
        let currentSlide = 1;
        const totalSlides = 6;

        function nextSlide() {
            if (currentSlide < totalSlides) {
                const current = document.getElementById(`slide${currentSlide}`);
                current.classList.remove('visible');
                currentSlide++;
                const next = document.getElementById(`slide${currentSlide}`);
                next.classList.add('visible');
            }
        }

        function restart() {
            const current = document.getElementById(`slide${currentSlide}`);
            current.classList.remove('visible');
            currentSlide = 1;
            const first = document.getElementById(`slide${currentSlide}`);
            first.classList.add('visible');
        }
    </script>
</body>
</html>
