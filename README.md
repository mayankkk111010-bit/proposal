<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>🎂 Happy Birthday MY LOVE !</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            min-height: 100vh;
            overflow-x: hidden;
            font-family: "Poppins", "Segoe UI", sans-serif;
            color: white;

            background:
                radial-gradient(circle at top left, #ff4ecd55, transparent 35%),
                radial-gradient(circle at bottom right, #6c63ff66, transparent 35%),
                linear-gradient(135deg, #17002b, #3b0754, #12002b);

            display: flex;
            justify-content: center;
            align-items: center;
            padding: 30px;
        }

        /* Main Card */
        .birthday-card {
            position: relative;
            width: 100%;
            max-width: 850px;
            padding: 50px 30px;
            text-align: center;

            background: rgba(255, 255, 255, 0.10);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 30px;

            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);

            box-shadow:
                0 20px 60px rgba(0, 0, 0, 0.4),
                inset 0 0 30px rgba(255,255,255,0.05);

            z-index: 10;
        }

        /* Heading */
        .birthday-card h1 {
            font-size: clamp(40px, 8vw, 80px);
            margin-bottom: 10px;

            background: linear-gradient(
                90deg,
                #ff8bd8,
                #fff,
                #ffd166,
                #ff8bd8
            );

            background-size: 300%;
            -webkit-background-clip: text;
            color: transparent;

            animation: gradientMove 5s linear infinite;
        }

        @keyframes gradientMove {
            0% {
                background-position: 0%;
            }

            100% {
                background-position: 300%;
            }
        }

        .subtitle {
            font-size: 20px;
            opacity: 0.9;
            margin-bottom: 30px;
        }

        /* Name */
        .name {
            font-size: clamp(30px, 6vw, 55px);
            color: #ffd166;
            text-shadow:
                0 0 10px #ffd166,
                0 0 30px #ff9f1c;

            margin: 15px 0;
        }

        /* Cake */
        .cake {
            position: relative;
            width: 180px;
            height: 130px;
            margin: 40px auto 30px;
        }

        .cake-body {
            position: absolute;
            bottom: 0;
            left: 10px;

            width: 160px;
            height: 80px;

            background: linear-gradient(
                #ff8fab,
                #ff4d6d
            );

            border-radius: 15px 15px 25px 25px;

            box-shadow:
                0 10px 30px rgba(255, 77, 109, 0.5);
        }

        .cake-top {
            position: absolute;
            top: 35px;
            left: 5px;

            width: 170px;
            height: 35px;

            background: #fff0f3;
            border-radius: 50%;
        }

        .candle {
            position: absolute;
            top: 0;
            left: 80px;

            width: 20px;
            height: 45px;

            background: repeating-linear-gradient(
                45deg,
                #ffffff 0px,
                #ffffff 8px,
                #ff4d6d 8px,
                #ff4d6d 16px
            );

            border-radius: 5px;
        }

        .flame {
            position: absolute;
            top: -25px;
            left: 3px;

            width: 14px;
            height: 22px;

            background: #ffd166;
            border-radius: 50% 50% 50% 0;

            transform: rotate(-45deg);

            box-shadow:
                0 0 10px #ffd166,
                0 0 25px #ff9f1c;

            animation: flicker 0.5s infinite alternate;
        }

        @keyframes flicker {
            from {
                transform: rotate(-45deg) scale(1);
            }

            to {
                transform: rotate(-45deg) scale(1.15);
            }
        }

        /* Message */
        .message {
            max-width: 650px;
            margin: 20px auto;

            font-size: 18px;
            line-height: 1.8;

            color: #f8eaff;
        }

        /* Buttons */
        .buttons {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 30px;
        }

        button {
            border: none;
            padding: 14px 25px;

            border-radius: 50px;

            font-size: 16px;
            font-weight: bold;

            cursor: pointer;

            color: white;

            background: linear-gradient(
                135deg,
                #ff4ecd,
                #6c63ff
            );

            box-shadow:
                0 8px 25px rgba(255, 78, 205, 0.35);

            transition: 0.3s;
        }

        button:hover {
            transform: translateY(-5px) scale(1.05);

            box-shadow:
                0 12px 35px rgba(255, 78, 205, 0.6);
        }

        /* Countdown */
        .countdown {
            margin-top: 30px;

            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }

        .time-box {
            min-width: 80px;
            padding: 15px;

            background: rgba(255,255,255,0.1);
            border-radius: 15px;

            border: 1px solid rgba(255,255,255,0.15);
        }

        .time-box span {
            display: block;
            font-size: 28px;
            font-weight: bold;
            color: #ffd166;
        }

        .time-box small {
            opacity: 0.8;
        }

        /* Balloons */
        .balloon {
            position: fixed;

            width: 55px;
            height: 70px;

            border-radius: 50%;

            z-index: 1;

            animation: floatBalloon linear infinite;
        }

        .balloon::after {
            content: "";
            position: absolute;

            width: 2px;
            height: 100px;

            background: rgba(255,255,255,0.5);

            left: 50%;
            top: 68px;
        }

        .balloon:nth-child(1) {
            left: 5%;
            background: #ff4d6d;
            animation-duration: 8s;
        }

        .balloon:nth-child(2) {
            left: 20%;
            background: #ffd166;
            animation-duration: 10s;
            animation-delay: 2s;
        }

        .balloon:nth-child(3) {
            right: 20%;
            background: #06d6a0;
            animation-duration: 9s;
            animation-delay: 1s;
        }

        .balloon:nth-child(4) {
            right: 5%;
            background: #6c63ff;
            animation-duration: 11s;
            animation-delay: 3s;
        }

        @keyframes floatBalloon {
            from {
                transform: translateY(110vh) rotate(-5deg);
            }

            to {
                transform: translateY(-150px) rotate(5deg);
            }
        }

        /* Surprise */
        #surprise {
            display: none;

            margin-top: 25px;

            font-size: 25px;
            font-weight: bold;

            color: #ffd166;

            animation: pop 0.6s ease;
        }

        @keyframes pop {
            0% {
                transform: scale(0);
            }

            70% {
                transform: scale(1.15);
            }

            100% {
                transform: scale(1);
            }
        }

        /* Mobile */
        @media (max-width: 600px) {

            body {
                padding: 15px;
            }

            .birthday-card {
                padding: 35px 20px;
            }

            .subtitle {
                font-size: 16px;
            }

            .message {
                font-size: 16px;
            }

            .balloon {
                width: 40px;
                height: 55px;
            }
        }
    </style>
</head>

<body>

    <!-- Balloons -->
    <div class="balloon"></div>
    <div class="balloon"></div>
    <div class="balloon"></div>
    <div class="balloon"></div>

    <!-- Birthday Card -->
    <div class="birthday-card">

        <h1>🎉 HAPPYYYY BIRTHDAY MERIIII PYARIIII NAINA MERII CUTE NIHARIKAAA! 🎉</h1>

        <p class="subtitle">
         <i>   Today is your Very special day ❤️🥺💋💗✨</i>
        </p>

        <div class="name">
            🎂MY DEAR BABUUUU 🎂❤️😭🥺🥹💗💕
        </div>


        <!-- Cake -->
        <div class="cake">
            <div class="candle">
                <div class="flame"></div>
            </div>

            <div class="cake-top"></div>

            <div class="cake-body"></div>

        </div>

        <p class="message">
           <b>💖YOU ARE MY CUTIE PIE MY CUTE GIRL I LOVE YOU SOO MUCHHH MERA KUCHUU PUCHUU MERAA BAACHAAA UMMAAA 😭😭😭🥺💋💗💕💖<br> YOU ARE MY CUTE WIFEYYYYYYY AWWWWWWWWWWWWWWWW YAARRRRRRRRRRRRR HAYEEEEEEEEEEEEE MEREEEEEEEEEEE BABUUUUUU KA BIRTHDAYYYYYY❤️😍😭😭🥺🥹🥰😘😍💋💋💗💕 </b>
            <br>
            <b>🥳 HAPPY BIRTHDAY MERAAA BABUUU MERI UMER TUJKO LAG JAYEEEE MERA BABUUUUUU AWWWWWWWWWWW IAM SOOOO HAPPPYYYYYYYYYY❤️😍😭😭🥺🥹🥰😘😍💋💋💗💕 🥳
        </p>

        <!-- Countdown -->
        <div class="countdown">

            <div class="time-box">
                <span id="days">00</span>
                <small>Days</small>
            </div>

            <div class="time-box">
                <span id="hours">00</span>
                <small>Hours</small>
            </div>

            <div class="time-box">
                <span id="minutes">00</span>
                <small>Minutes</small>
            </div>

            <div class="time-box">
                <span id="seconds">00</span>
                <small>Seconds</small>
            </div>

        </div>

        <!-- Buttons -->
        <div class="buttons">

            <button onclick="surprise()">
                🎁 Open Surprise
            </button>

            <button onclick="createConfetti()">
                🎉 More Confetti
            </button>

        </div>

        <div id="surprise">
            I love you sooo muchh babyyyy may your birthday be filled with happiness and lot's of lovee you aree soo special person 🫠 hayeee you aree veryy cuteee lovely and very very cuteeeee you aree sooo beautiful in the world you are soo pretty cute gorgeous and beautiful hayeeee ummaa bhagwan aapka yee birthday sabse best ho aur aapki life is birthday se khushiyo se bhar jayeee aur bohot khusiyan aapki life me rahe aur kabhi bhi aapko dhuk na mile aap hamesa khus raho aur jo bhi goals aapne banaye hai wo sare achieve ho jaye aur aap hamesa ek Happy life jeeyo aur khus raho aur haaaa 🥺🥺🥺 mere sathh hi rahoo samji 🥺🥺🥺 dur mat jana samji naa 🥺🥺 merii cutee babu 🥺🥺 i loveee youuu soo muchh babyyy 😭😭😭😭😭😭😭😭😭 i got soo emotional this dayy 😭😭😭😭😭😭 I can't explain and express babuu 😭😭😭 youu aree sooooooooooo cuteee babuuu 😭😭😭😭😭 ummaaa ummaaa ummaaaaaa 💋💋💋💋💋💋💋💋💋💋 i loveee youu soo much babuu hamesa khuss rehnaa aur meri rehna aur aapko jab bhi meri koi baat buri lage mujhe tab hi datna marna aur samjana sorry babu for my stupid things and mistakes 🥺🥺🥺🙏🏻🙏🏻🙏🏻🙏🏻🙏🏻 maaaf kar dena babuu soorry 🥺🥺 mai aapke liye bohot acha banunga pakkaa aur hamesa aapko khus rakne ki kois karungaa aapke liye hamesa stand lunga aur sath rahunga aur aapke liye loyal rahunga aur aapke sath rahunga aapke liye hamesa mehnat karunga 🥺🥺🥺💗🫶🏻💋🫂

    </div>

    <script>

        /* =========================
           SURPRISE BUTTON
        ========================= */

        function surprise() {

            const surpriseBox = document.getElementById("surprise");

            surpriseBox.style.display = "block";

            createConfetti();
            createConfetti();
        }


        /* =========================
           CONFETTI
        ========================= */

        function createConfetti() {

            const colors = [
                "#ff4d6d",
                "#ffd166",
                "#06d6a0",
                "#6c63ff",
                "#ff4ecd",
                "#ffffff"
            ];

            for (let i = 0; i < 100; i++) {

                const confetti = document.createElement("div");

                confetti.style.position = "fixed";
                confetti.style.width = "8px";
                confetti.style.height = "14px";

                confetti.style.background =
                    colors[Math.floor(Math.random() * colors.length)];

                confetti.style.left =
                    Math.random() * 100 + "vw";

                confetti.style.top = "-20px";

                confetti.style.zIndex = "999";

                confetti.style.transform =
                    `rotate(${Math.random() * 360}deg)`;

                document.body.appendChild(confetti);

                const duration =
                    Math.random() * 3 + 2;

                confetti.animate(
                    [
                        {
                            transform:
                                `translateY(0) rotate(0deg)`
                        },

                        {
                            transform:
                                `translateY(110vh) rotate(720deg)`
                        }
                    ],
                    {
                        duration: duration * 1000,
                        easing: "linear"
                    }
                );

                setTimeout(() => {
                    confetti.remove();
                }, duration * 1000);
            }
        }


        /* =========================
           BIRTHDAY COUNTDOWN
        ========================= */

        // Change this date to the birthday
        const birthday = new Date("October 11, 2026 00:00:00").getTime();

        function updateCountdown() {

            const now = new Date().getTime();

            const distance = birthday - now;

            if (distance <= 0) {

                document.getElementById("days").innerText = "00";
                document.getElementById("hours").innerText = "00";
                document.getElementById("minutes").innerText = "00";
                document.getElementById("seconds").innerText = "00";

                createConfetti();

                return;
            }

            const days =
                Math.floor(
                    distance / (1000 * 60 * 60 * 24)
                );

            const hours =
                Math.floor(
                    (distance %
                        (1000 * 60 * 60 * 24))
                    /
                    (1000 * 60 * 60)
                );

            const minutes =
                Math.floor(
                    (distance %
                        (1000 * 60 * 60))
                    /
                    (1000 * 60)
                );

            const seconds =
                Math.floor(
                    (distance %
                        (1000 * 60))
                    /
                    1000
                );

            document.getElementById("days").innerText =
                String(days).padStart(2, "0");

            document.getElementById("hours").innerText =
                String(hours).padStart(2, "0");

            document.getElementById("minutes").innerText =
                String(minutes).padStart(2, "0");

            document.getElementById("seconds").innerText =
                String(seconds).padStart(2, "0");
        }

        setInterval(updateCountdown, 1000);

        updateCountdown();


        /* =========================
           START CONFETTI
        ========================= */

        setTimeout(() => {
            createConfetti();
        }, 1000);

    </script>

</body>
</html>

