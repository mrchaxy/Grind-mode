<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Grind Mode</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

    <style>
        body {
            margin: 0;
            min-height: 100vh;
            background: linear-gradient(120deg, #050505, #0f0f0f, #050505);
            background-size: 400% 400%;
            animation: bgMove 10s ease infinite;
            color: #ffffff;
            display: flex;
            align-items: center;
            justify-content: center;
            font-family: Arial, Helvetica, sans-serif;
            text-align: center;
        }

        @keyframes bgMove {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .container {
            width: 90%;
            max-width: 520px;
            padding: 30px 20px;
            font-weight: 900;
        }

        h1 {
            font-size: 2.4rem;
            margin-bottom: 25px;
            text-shadow: 0 0 20px rgba(0, 255, 200, 0.4);
        }

        .typing {
            font-size: 1.15rem;
            line-height: 1.6;
            min-height: 70px;
            margin-bottom: 25px;
        }

        .buttons {
            display: flex;
            flex-direction: column;
            gap: 18px;
        }

        .btn {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 12px;
            padding: 16px;
            font-size: 1.15rem;
            font-weight: 900;
            border-radius: 50px;
            text-decoration: none;
            color: #fff;
            letter-spacing: 0.5px;
            animation: pulse 2s infinite;
            transition: transform 0.25s ease;
        }

        .btn:hover {
            transform: scale(1.06);
        }

        .youtube {
            background: #ff0000;
            box-shadow: 0 0 25px rgba(255, 0, 0, 0.7);
        }

        .instagram {
            background: linear-gradient(45deg, #f58529, #dd2a7b, #8134af, #515bd4);
            box-shadow: 0 0 25px rgba(221, 42, 123, 0.7);
            animation-delay: 0.4s;
        }

        i {
            font-size: 1.5rem;
        }

        @keyframes pulse {
            0% { box-shadow: 0 0 15px rgba(255,255,255,0.4); }
            50% { box-shadow: 0 0 30px rgba(255,255,255,0.9); }
            100% { box-shadow: 0 0 15px rgba(255,255,255,0.4); }
        }

        @media (max-width: 480px) {
            h1 { font-size: 2.1rem; }
            .typing { font-size: 1.05rem; }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>GRIND MODE ACTIVATED 💻</h1>

        <div class="typing" id="typing"></div>

        <div class="buttons">
            <a class="btn youtube"
               href="https://www.youtube.com/channel/UCLEByF7kvKLg_XckmVeTAOg"
               target="_blank">
                <i class="fab fa-youtube"></i>
                WATCH ON YOUTUBE
            </a>

            <a class="btn instagram"
               href="https://www.instagram.com/mr_chaxy/reels/?hl=en"
               target="_blank">
                <i class="fab fa-instagram"></i>
                WATCH ON INSTAGRAM
            </a>
        </div>
    </div>

    <script>
        const text = 
            "I AM CURRENTLY IN GRIND MODE.\n" +
            "TALK TO YOU LATER WHEN I FIND TIME.\n\n" +
            "BUT YOU CAN WATCH MY VIDEOS WHILE YOU WAIT 👇";

        const typingElement = document.getElementById("typing");
        let index = 0;

        function typeText() {
            if (index < text.length) {
                typingElement.innerHTML += 
                    text[index] === "\n" ? "<br>" : text[index];
                index++;
                setTimeout(typeText, 40);
            }
        }

        typeText();
    </script>
</body>
</html>
