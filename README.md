<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Grind Mode</title>
</head>
<body style="background:black;color:white;text-align:center;padding-top:40vh;font-family:Arial;">
    <h1>GRIND MODE ACTIVATED 💻</h1>
    <p>I am currently in grind mode. Talk to you later.</p>
</body>
</html>


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
                    text[index] === "\\n" ? "<br>" : text[index];
                index++;
                setTimeout(typeText, 40);
            }
        }

        typeText();
    </script>
</body>
</html>
