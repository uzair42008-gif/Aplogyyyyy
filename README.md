<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>I'm Really Sorry ❤️</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Comic Sans MS', 'Comic Sans', cursive;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(-45deg, #ee7752, #e73c7e, #ff69b4, #ff1493, #ff69b4, #e73c7e);
            background-size: 400% 400%;
            animation: gradientShift 8s ease infinite;
            overflow: hidden;
            position: relative;
        }

        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .bg-heart {
            position: fixed;
            font-size: 2em;
            opacity: 0.15;
            animation: floatAround 15s ease-in-out infinite;
            pointer-events: none;
            color: #fff;
        }

        @keyframes floatAround {
            0%, 100% {
                transform: translate(0, 0) rotate(0deg);
            }
            25% {
                transform: translate(100px, -100px) rotate(90deg);
            }
            50% {
                transform: translate(200px, 50px) rotate(180deg);
            }
            75% {
                transform: translate(-50px, -50px) rotate(270deg);
            }
        }

        .container {
            text-align: center;
            padding: 50px 40px;
            background: rgba(255, 255, 255, 0.98);
            border-radius: 35px;
            box-shadow: 0 25px 70px rgba(255, 105, 180, 0.5);
            max-width: 650px;
            width: 90%;
            animation: floatIn 1s ease-out;
            border: 3px solid rgba(255, 105, 180, 0.3);
            position: relative;
            z-index: 10;
        }

        @keyframes floatIn {
            from {
                opacity: 0;
                transform: translateY(-50px) scale(0.9);
            }
            to {
                opacity: 1;
                transform: translateY(0) scale(1);
            }
        }

        #mainText {
            font-size: 2.8em;
            color: #e73c7e;
            margin-bottom: 50px;
            font-weight: bold;
            text-shadow: 3px 3px 6px rgba(255, 105, 180, 0.3);
            animation: pulse 2s ease-in-out infinite;
            line-height: 1.5;
        }

        @media (max-width: 768px) {
            #mainText {
                font-size: 2em;
            }
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.08); }
        }

        .buttons {
            display: flex;
            gap: 25px;
            justify-content: center;
            flex-wrap: wrap;
            margin-bottom: 20px;
            min-height: 200px;
            align-items: center;
            position: relative;
            padding: 20px;
        }

        @media (max-width: 768px) {
            .buttons {
                min-height: 350px;
                flex-direction: column;
            }
        }

        button {
            font-family: 'Comic Sans MS', 'Comic Sans', cursive;
            font-size: 1.4em;
            padding: 20px 40px;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s ease;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
            position: relative;
        }

        @media (max-width: 768px) {
            button {
                font-size: 1.2em;
                padding: 16px 30px;
            }
        }

        #yesBtn {
            background: linear-gradient(135deg, #ff69b4, #ff1493);
            color: white;
            position: relative;
            z-index: 5;
        }

        #yesBtn:hover {
            transform: translateY(-8px) scale(1.1);
            box-shadow: 0 15px 40px rgba(255, 20, 147, 0.5);
        }

        #noBtn {
            background: linear-gradient(135deg, #ffb6c1, #ff69b4);
            color: #fff;
            position: absolute;
            transition: all 0.15s ease-out;
            z-index: 10;
        }

        #noBtn:hover {
            transform: scale(1.05);
        }

        button:active {
            transform: translateY(-2px) scale(1.02);
        }

        #emojiContainer {
            font-size: 3.5em;
            margin-top: 30px;
            animation: bounce 1s ease infinite;
            letter-spacing: 10px;
        }

        @media (max-width: 768px) {
            #emojiContainer {
                font-size: 2.5em;
                letter-spacing: 5px;
            }
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-25px); }
        }

        .hidden {
            display: none;
        }

        .heart {
            position: fixed;
            font-size: 2.5em;
            animation: floatUp 4s ease-in-out;
            pointer-events: none;
            z-index: 1000;
        }

        @keyframes floatUp {
            0% {
                opacity: 1;
                transform: translateY(0) rotate(0deg);
            }
            100% {
                opacity: 0;
                transform: translateY(-1000px) rotate(360deg);
            }
        }

        .shake {
            animation: shake 0.5s;
        }

        @keyframes shake {
            0%, 100% { transform: translateX(0); }
            25% { transform: translateX(-10px) rotate(-5deg); }
            75% { transform: translateX(10px) rotate(5deg); }
        }

        #clickCount {
            margin-top: 20px;
            font-size: 1.1em;
            color: #e73c7e;
            font-weight: bold;
            min-height: 30px;
        }

        @media (max-width: 768px) {
            #clickCount {
                font-size: 1em;
            }
        }

        .sparkle {
            position: fixed;
            width: 10px;
            height: 10px;
            background: white;
            border-radius: 50%;
            pointer-events: none;
            animation: sparkleAnim 1s ease-out forwards;
            z-index: 999;
        }

        @keyframes sparkleAnim {
            0% {
                opacity: 1;
                transform: scale(0);
            }
            50% {
                opacity: 1;
                transform: scale(1);
            }
            100% {
                opacity: 0;
                transform: scale(0);
            }
        }
    </style>
</head>
<body>
    <div class="bg-heart" style="top: 10%; left: 10%; animation-delay: 0s;">❤️</div>
    <div class="bg-heart" style="top: 70%; left: 80%; animation-delay: 2s;">💖</div>
    <div class="bg-heart" style="top: 30%; left: 85%; animation-delay: 4s;">💕</div>
    <div class="bg-heart" style="top: 60%; left: 15%; animation-delay: 6s;">💗</div>
    <div class="bg-heart" style="top: 20%; left: 50%; animation-delay: 8s;">💝</div>

    <div class="container">
        <div id="mainText">I'm really sorry ❤️<br>Please forgive me 🥺</div>
        <div class="buttons">
            <button id="yesBtn">Okay baby, I forgive you 💖</button>
            <button id="noBtn">No, I'm still angry 😠</button>
        </div>
        <div id="clickCount"></div>
        <div id="emojiContainer" class="hidden"></div>
    </div>

    <script>
        const mainText = document.getElementById('mainText');
        const yesBtn = document.getElementById('yesBtn');
        const noBtn = document.getElementById('noBtn');
        const emojiContainer = document.getElementById('emojiContainer');
        const clickCount = document.getElementById('clickCount');
        const buttonsContainer = document.querySelector('.buttons');

        /* ============================================================
          EDIT YOUR CUSTOM APOLOGY LINES HERE!
          You can use <br> to create a line break/new line.
          ============================================================
        */
        const sorryMessages = [
            "I'm really sorry ❤️<br>Please forgive me 🥺",
            "I promise I will listen to you more carefully next time 🌸",
            "I hate it when we're not talking. I miss you so much! 🥺❤️",
            "I am completely at fault here, please forgive your idiot 🤡💕",
            "My day is 0% complete without you. Let's make up? ✨",
            "Look how much effort I put into this page just to hear you say yes! 👉👈",
            "I'll give you unlimited hugs and back scratches forever 👑💖",
            "I'm so sorry for being stubborn. I love you the most! 🥰",
            "Can we please erase the anger and replace it with cuddles? 🐻❤️",
            "I'm deeply sorry, let me make it up to you with food? 🍕🍓",
            "Pretty please with a million cherries on top? 🍒🥺",
            "You are my absolute favorite person. I'm sorry for messing up 🌎💞",
            "Please stop clicking 'No', look how small the poor button is getting! 😂",
            "Okay, seriously, I am incredibly sorry. I love you to the moon and back 🌙✨",
            "I promise to be a better partner for you every single day 💍❤️"
        ];

        let currentMessageIndex = 0;
        let noClickCount = 0;
        const isMobile = /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent);

        // Update default opening message to match the first item in the array
        mainText.innerHTML = sorryMessages[0];

        function createSparkle(x, y) {
            for (let i = 0; i < 5; i++) {
                const sparkle = document.createElement('div');
                sparkle.className = 'sparkle';
                sparkle.style.left = x + (Math.random() - 0.5) * 50 + 'px';
                sparkle.style.top = y + (Math.random() - 0.5) * 50 + 'px';
                document.body.appendChild(sparkle);
                setTimeout(() => sparkle.remove(), 1000);
            }
        }

        function createHeart() {
            const heart = document.createElement('div');
            heart.className = 'heart';
            heart.textContent = ['❤️', '💖', '💕', '💗', '💝', '🥰', '😍'][Math.floor(Math.random() * 7)];
            heart.style.left = Math.random() * window.innerWidth + 'px';
            heart.style.top = window.innerHeight + 'px';
            document.body.appendChild(heart);
            setTimeout(() => heart.remove(), 4000);
        }

        function moveNoButton() {
            const rect = buttonsContainer.getBoundingClientRect();
            const btnRect = noBtn.getBoundingClientRect();
            const yesRect = yesBtn.getBoundingClientRect();
            const maxX = rect.width - btnRect.width - 20;
            const maxY = rect.height - btnRect.height - 20;
            
            let newX, newY;
            let attempts = 0;
            const maxAttempts = 50;
            
            do {
                newX = Math.random() * maxX + 10;
                newY = Math.random() * maxY + 10;
                attempts++;
                
                const noLeft = rect.left + newX;
                const noRight = noLeft + btnRect.width;
                const noTop = rect.top + newY;
                const noBottom = noTop + btnRect.height;
                
                const yesLeft = yesRect.left;
                const yesRight = yesRect.right;
                const yesTop = yesRect.top;
                const yesBottom = yesRect.bottom;
                
                const padding = 30;
                
                const overlaps = !(
                    noRight + padding < yesLeft ||
                    noLeft - padding > yesRight ||
                    noBottom + padding < yesTop ||
                    noTop - padding > yesBottom
                );
                
                if (!overlaps || attempts >= maxAttempts) {
                    break;
                }
            } while (true);
            
            noBtn.style.left = newX + 'px';
            noBtn.style.top = newY + 'px';
            
            createSparkle(btnRect.left + btnRect.width/2, btnRect.top + btnRect.height/2);
            
            noClickCount++;
            const newScale = Math.max(0.3, 1 - (noClickCount * 0.1));
            noBtn.style.transform = `scale(${newScale})`;
        }

        function initNoButton() {
            const isMobileView = window.innerWidth <= 768;
            noBtn.style.left = isMobileView ? '50%' : '70%';
            noBtn.style.top = isMobileView ? '70%' : '50%';
            noBtn.style.transform = 'translate(-50%, -50%) scale(1)';
            noClickCount = 0;
        }

        initNoButton();
        window.addEventListener('resize', initNoButton);

        if (!isMobile) {
            noBtn.addEventListener('mouseenter', function() {
                moveNoButton();
                currentMessageIndex = (currentMessageIndex + 1) % sorryMessages.length;
                mainText.innerHTML = sorryMessages[currentMessageIndex];
                mainText.classList.add('shake');
                setTimeout(() => mainText.classList.remove('shake'), 500);
                
                if (noClickCount <= 5) {
                    clickCount.innerHTML = `Come on... just click YES! 🥺 (Attempts: ${noClickCount})`;
                } else if (noClickCount <= 10) {
                    clickCount.innerHTML = `Please baby! I'm begging you! 😭 (Attempts: ${noClickCount})`;
                } else {
                    clickCount.innerHTML = `I can do this all day! 💪❤️ (Attempts: ${noClickCount})`;
                }
                
                createHeart();
            });
        }

        noBtn.addEventListener('click', function(e) {
            e.preventDefault();
            moveNoButton();
            
            currentMessageIndex = (currentMessageIndex + 1) % sorryMessages.length;
            mainText.innerHTML = sorryMessages[currentMessageIndex];
            
            mainText.classList.add('shake');
            setTimeout(() => mainText.classList.remove('shake'), 500);

            if (noClickCount <= 5) {
                clickCount.innerHTML = `Come on... just click YES! 🥺 (Attempts: ${noClickCount})`;
            } else if (noClickCount <= 10) {
                clickCount.innerHTML = `Please baby! I'm begging you! 😭 (Attempts: ${noClickCount})`;
            } else {
                clickCount.innerHTML = `I can do this all day! 💪❤️ (Attempts: ${noClickCount})`;
            }

            createHeart();
        });

        yesBtn.addEventListener('click', function() {
            mainText.innerHTML = "Yay! You forgave me! 😍💖🥳";
            emojiContainer.innerHTML = "😊❤️💃🎉✨🥰💕🌟🎊💖🌹😘";
            emojiContainer.classList.remove('hidden');
            clickCount.innerHTML = "I LOVE YOU SO MUCH! ❤️❤️❤️";
            buttonsContainer.style.display = 'none';

            for (let i = 0; i < 30; i++) {
                setTimeout(() => createHeart(), i * 150);
            }

            document.body.style.background = 'linear-gradient(-45deg, #ff69b4, #ff1493, #ff69b4, #ffc0cb, #ff69b4, #ff1493)';
        });

        setInterval(() => {
            if (noClickCount > 3 && buttonsContainer.style.display !== 'none') {
                yesBtn.style.transform = `translateY(-8px) scale(${1.1 + (noClickCount * 0.05)})`;
            }
        }, 100);
    </script>
</body>
</html>

