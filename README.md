
html_content = r'''<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A Little Pact Between Saye-e-Dil and Rana Bilal Naveed</title>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,400&family=Great+Vibes&family=Playfair+Display:ital,wght@0,400;0,600;1,400&display=swap" rel="stylesheet">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        html { scroll-behavior: smooth; }
        body {
            font-family: 'Cormorant Garamond', serif;
            min-height: 100vh;
            overflow-x: hidden;
            color: #fff;
            background: #0a0a0a;
        }
        .bg-container {
            position: fixed;
            top: 0; left: 0;
            width: 100%; height: 100%;
            z-index: 0;
            overflow: hidden;
        }
        .bg-image {
            width: 100%; height: 100%;
            object-fit: cover;
            filter: brightness(0.4) saturate(1.2);
            animation: breathe 10s ease-in-out infinite;
        }
        @keyframes breathe {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }
        .bg-overlay {
            position: fixed;
            top: 0; left: 0;
            width: 100%; height: 100%;
            background:
                radial-gradient(ellipse at 30% 20%, rgba(255, 215, 0, 0.15) 0%, transparent 50%),
                radial-gradient(ellipse at 70% 80%, rgba(255, 105, 180, 0.15) 0%, transparent 50%),
                linear-gradient(to bottom, rgba(0,0,0,0.3) 0%, rgba(0,0,0,0.5) 100%);
            z-index: 1;
            pointer-events: none;
        }
        .particles {
            position: fixed;
            top: 0; left: 0;
            width: 100%; height: 100%;
            pointer-events: none;
            z-index: 2;
        }
        .particle {
            position: absolute;
            width: 3px; height: 3px;
            background: rgba(255, 255, 255, 0.8);
            border-radius: 50%;
            box-shadow: 0 0 10px rgba(255, 255, 255, 0.8), 0 0 20px rgba(255, 215, 0, 0.5);
            animation: float 20s infinite;
        }
        @keyframes float {
            0%, 100% { transform: translateY(100vh) translateX(0) rotate(0deg); opacity: 0; }
            10% { opacity: 1; }
            90% { opacity: 1; }
            100% { transform: translateY(-100vh) translateX(100px) rotate(720deg); opacity: 0; }
        }
        .firefly {
            position: absolute;
            width: 4px; height: 4px;
            background: #ffd700;
            border-radius: 50%;
            box-shadow: 0 0 20px #ffd700, 0 0 40px #ffd700;
            animation: firefly 8s ease-in-out infinite;
        }
        @keyframes firefly {
            0%, 100% { opacity: 0; transform: translate(0, 0) scale(0); }
            20% { opacity: 1; }
            50% { opacity: 1; transform: translate(30px, -50px) scale(1); }
            80% { opacity: 0.5; }
        }
        .container {
            position: relative;
            z-index: 10;
            max-width: 850px;
            margin: 0 auto;
            padding: 40px 20px;
        }
        .intro-section {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 60px 20px;
            animation: fadeIn 2s ease-out;
        }
        .intro-heart {
            font-size: 4rem;
            animation: heartbeat 2s ease-in-out infinite;
            margin-bottom: 30px;
            filter: drop-shadow(0 0 20px rgba(255, 215, 0, 0.5));
        }
        @keyframes heartbeat {
            0%, 100% { transform: scale(1); }
            25% { transform: scale(1.1); }
            50% { transform: scale(1); }
            75% { transform: scale(1.05); }
        }
        .intro-title {
            font-family: 'Great Vibes', cursive;
            font-size: 3.5rem;
            background: linear-gradient(45deg, #ffd700, #fff, #ff69b4, #ffd700);
            background-size: 300% 300%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: shimmer 4s ease infinite;
            text-shadow: 0 0 40px rgba(255, 215, 0, 0.3);
            margin-bottom: 20px;
        }
        @keyframes shimmer {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        .intro-subtitle {
            font-size: 1.4rem;
            color: rgba(255, 255, 255, 0.9);
            max-width: 600px;
            line-height: 1.8;
            text-shadow: 0 2px 10px rgba(0,0,0,0.5);
            margin-bottom: 15px;
        }
        .tiny-note {
            font-size: 1.1rem;
            color: rgba(255, 215, 0, 0.8);
            font-style: italic;
            margin-bottom: 10px;
        }
        .warning-text {
            font-size: 1rem;
            color: rgba(255, 105, 180, 0.9);
            margin-bottom: 30px;
            max-width: 500px;
            line-height: 1.6;
        }
        .scroll-hint {
            margin-top: 40px;
            font-size: 0.9rem;
            color: rgba(255, 215, 0, 0.7);
            animation: bounce 2s infinite;
        }
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(10px); }
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .question-section {
            padding: 60px 0;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        .section-title {
            font-family: 'Playfair Display', serif;
            font-size: 2rem;
            text-align: center;
            margin-bottom: 30px;
            color: #ffd700;
            text-shadow: 0 0 20px rgba(255, 215, 0, 0.3);
        }
        .section-title::before, .section-title::after {
            content: '✦';
            margin: 0 15px;
            color: rgba(255, 215, 0, 0.5);
        }
        .question-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(20px);
            border-radius: 25px;
            padding: 35px;
            margin-bottom: 25px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.3), inset 0 1px 0 rgba(255, 255, 255, 0.1);
            transition: all 0.6s cubic-bezier(0.4, 0, 0.2, 1);
            display: none;
            position: relative;
            overflow: hidden;
            animation: cardAppear 0.8s ease-out;
        }
        .question-card::before {
            content: '';
            position: absolute;
            top: -50%; left: -50%;
            width: 200%; height: 200%;
            background: radial-gradient(circle, rgba(255, 215, 0, 0.1) 0%, transparent 70%);
            opacity: 0;
            transition: opacity 0.5s ease;
        }
        .question-card.active {
            display: block;
            opacity: 1;
            border-color: rgba(255, 215, 0, 0.3);
        }
        .question-card.active::before { opacity: 1; }
        .question-card.answered { display: none; }
        @keyframes cardAppear {
            from { opacity: 0; transform: translateY(50px) scale(0.9); }
            to { opacity: 1; transform: translateY(0) scale(1); }
        }
        .question-number {
            font-family: 'Great Vibes', cursive;
            font-size: 2.5rem;
            color: #ffd700;
            text-shadow: 0 0 20px rgba(255, 215, 0, 0.5);
            line-height: 1;
            margin-bottom: 15px;
        }
        .question-icon {
            font-size: 2.5rem;
            margin-bottom: 15px;
            animation: iconFloat 3s ease-in-out infinite;
        }
        @keyframes iconFloat {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
        .question-text {
            font-size: 1.3rem;
            line-height: 2;
            color: rgba(255, 255, 255, 0.95);
            margin-bottom: 35px;
            font-weight: 300;
        }
        .question-text .highlight { color: #ffd700; font-weight: 500; }
        .button-container {
            display: flex;
            gap: 25px;
            justify-content: center;
            flex-wrap: wrap;
            position: relative;
            padding: 20px 0;
            min-height: 80px;
        }
        .btn {
            padding: 18px 50px;
            border: none;
            border-radius: 50px;
            font-size: 1.2rem;
            font-family: 'Cormorant Garamond', serif;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        .btn-yes {
            background: linear-gradient(135deg, #ffd700, #ff69b4);
            color: #1a1a2e;
            box-shadow: 0 5px 20px rgba(255, 215, 0, 0.4);
            min-width: 120px;
        }
        .btn-yes:hover {
            transform: scale(1.08);
            box-shadow: 0 8px 30px rgba(255, 215, 0, 0.6);
        }
        .btn-no {
            background: linear-gradient(135deg, #ffd700, #ffec8b);
            color: #1a1a2e;
            border: 2px solid #ffd700;
            box-shadow: 0 5px 20px rgba(255, 215, 0, 0.3);
            transition: all 0.15s ease;
            min-width: 120px;
            position: relative;
        }
        .btn-no:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 25px rgba(255, 215, 0, 0.5);
        }
        .btn-no.running {
            position: absolute !important;
            transition: all 0.3s cubic-bezier(0.68, -0.55, 0.265, 1.55);
        }
        .fairy-laugh {
            position: fixed;
            font-size: 1.5rem;
            color: #ffd700;
            font-family: 'Great Vibes', cursive;
            pointer-events: none;
            z-index: 60;
            opacity: 0;
            text-shadow: 0 0 20px rgba(255, 215, 0, 0.8);
            white-space: nowrap;
        }
        .fairy-laugh.show {
            animation: laughAppear 2s ease-out forwards;
        }
        @keyframes laughAppear {
            0% { opacity: 0; transform: translateY(20px) scale(0.5); }
            20% { opacity: 1; transform: translateY(0) scale(1.1); }
            50% { opacity: 1; transform: translateY(-10px) scale(1); }
            80% { opacity: 0.8; transform: translateY(-20px) scale(0.9); }
            100% { opacity: 0; transform: translateY(-40px) scale(0.5); }
        }
        .fairy-container {
            position: fixed;
            top: 0; left: 0;
            width: 100%; height: 100%;
            pointer-events: none;
            z-index: 50;
            overflow: hidden;
        }
        .fairy {
            position: absolute;
            width: 120px; height: 140px;
            opacity: 0;
            filter: drop-shadow(0 0 20px rgba(255, 215, 0, 0.8));
        }
        .fairy svg { width: 100%; height: 100%; }
        .fairy-appear {
            animation: fairyAppear 4s ease-in-out forwards;
        }
        @keyframes fairyAppear {
            0% { opacity: 0; transform: translateY(100px) scale(0.3) rotate(-20deg); }
            15% { opacity: 1; transform: translateY(0) scale(1) rotate(5deg); }
            30% { transform: translateY(-30px) scale(1.1) rotate(-5deg); }
            50% { transform: translateY(-50px) scale(1) rotate(5deg); }
            70% { opacity: 1; transform: translateY(-80px) scale(0.9) rotate(-3deg); }
            100% { opacity: 0; transform: translateY(-150px) scale(0.5) rotate(0deg); }
        }
        .fairy-gift {
            position: absolute;
            font-size: 2.5rem;
            opacity: 0;
            animation: giftFloat 3s ease-out forwards;
            filter: drop-shadow(0 0 15px rgba(255, 215, 0, 0.8));
        }
        @keyframes giftFloat {
            0% { opacity: 0; transform: translateY(0) scale(0.5); }
            20% { opacity: 1; transform: translateY(-30px) scale(1.2); }
            50% { opacity: 1; transform: translateY(-60px) scale(1); }
            100% { opacity: 0; transform: translateY(-100px) scale(0.3); }
        }
        .fairy-dust {
            position: absolute;
            width: 4px; height: 4px;
            background: radial-gradient(circle, #ffd700, #ff69b4);
            border-radius: 50%;
            box-shadow: 0 0 10px #ffd700;
            animation: dustFloat 2s ease-out forwards;
        }
        @keyframes dustFloat {
            0% { opacity: 1; transform: translate(0, 0) scale(1); }
            100% { opacity: 0; transform: translate(var(--dx), var(--dy)) scale(0); }
        }
        .final-section {
            min-height: 100vh;
            display: none;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 60px 20px;
            text-align: center;
            opacity: 0;
            transition: opacity 1.5s ease;
            position: relative;
        }
        .final-section.visible {
            display: flex;
            opacity: 1;
        }
        .final-heart {
            font-size: 5rem;
            animation: heartbeat 1.5s ease-in-out infinite;
            filter: drop-shadow(0 0 30px rgba(255, 215, 0, 0.6));
            margin-bottom: 20px;
        }
        .final-text {
            font-family: 'Great Vibes', cursive;
            font-size: 3.5rem;
            background: linear-gradient(45deg, #ffd700, #fff, #ff69b4);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: glow 3s ease-in-out infinite;
            margin-bottom: 15px;
        }
        @keyframes glow {
            0%, 100% { text-shadow: 0 0 20px rgba(255, 215, 0, 0.3); }
            50% { text-shadow: 0 0 40px rgba(255, 215, 0, 0.6), 0 0 60px rgba(255, 105, 180, 0.4); }
        }
        .final-subtext {
            font-size: 1.3rem;
            color: rgba(255, 255, 255, 0.8);
            font-style: italic;
        }
        .thumb-stamp-section {
            display: none;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            margin-top: 40px;
            animation: fadeIn 1s ease-out;
        }
        .thumb-stamp-section.visible { display: flex; }
        .stamp-pad {
            width: 200px; height: 200px;
            border-radius: 50%;
            background: radial-gradient(circle, #ff69b4, #ff1493);
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            box-shadow: 0 0 40px rgba(255, 105, 180, 0.5), inset 0 0 30px rgba(0,0,0,0.2);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        .stamp-pad:hover {
            transform: scale(1.05);
            box-shadow: 0 0 60px rgba(255, 105, 180, 0.7), inset 0 0 30px rgba(0,0,0,0.2);
        }
        .stamp-pad:active { transform: scale(0.95); }
        .stamp-pad-text {
            font-family: 'Great Vibes', cursive;
            font-size: 1.8rem;
            color: #fff;
            text-shadow: 0 2px 10px rgba(0,0,0,0.3);
            pointer-events: none;
        }
        .stamp-instruction {
            margin-top: 20px;
            font-size: 1.2rem;
            color: rgba(255, 255, 255, 0.8);
            font-style: italic;
        }
        .thumb-print {
            position: absolute;
            width: 80px; height: 100px;
            border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
            background: radial-gradient(ellipse at 30% 30%, #ff69b4, #ff1493, #8b0000);
            opacity: 0;
            transform: scale(2);
            pointer-events: none;
            filter: blur(1px);
        }
        .thumb-print.stamped {
            animation: stampAppear 0.6s ease-out forwards;
        }
        @keyframes stampAppear {
            0% { opacity: 0; transform: scale(2) rotate(-10deg); }
            50% { opacity: 0.9; transform: scale(0.9) rotate(5deg); }
            100% { opacity: 0.8; transform: scale(1) rotate(0deg); }
        }
        .disturb-text {
            font-family: 'Great Vibes', cursive;
            font-size: 2.5rem;
            color: #ffd700;
            margin-top: 30px;
            opacity: 0;
            text-shadow: 0 0 30px rgba(255, 215, 0, 0.6);
        }
        .disturb-text.show {
            animation: disturbAppear 1.5s ease-out forwards;
        }
        @keyframes disturbAppear {
            0% { opacity: 0; transform: translateY(30px) scale(0.8); }
            50% { opacity: 1; transform: translateY(-10px) scale(1.05); }
            100% { opacity: 1; transform: translateY(0) scale(1); }
        }
        .cute-fairy-final {
            font-size: 4rem;
            margin-top: 20px;
            opacity: 0;
            animation: fairyBounce 1s ease-in-out infinite;
        }
        .cute-fairy-final.show {
            opacity: 1;
            animation: fairyBounce 1s ease-in-out infinite, fadeIn 1s ease-out forwards;
        }
        @keyframes fairyBounce {
            0%, 100% { transform: translateY(0) rotate(-5deg); }
            50% { transform: translateY(-15px) rotate(5deg); }
        }
        .progress-container {
            position: fixed;
            top: 0; left: 0;
            width: 100%; height: 4px;
            background: rgba(255, 255, 255, 0.1);
            z-index: 100;
        }
        .progress-bar {
            height: 100%;
            background: linear-gradient(90deg, #ffd700, #ff69b4, #ffd700);
            background-size: 200% 100%;
            width: 0%;
            transition: width 0.6s cubic-bezier(0.4, 0, 0.2, 1);
            box-shadow: 0 0 20px rgba(255, 215, 0, 0.8);
            animation: progressShine 2s linear infinite;
        }
        @keyframes progressShine {
            0% { background-position: 0% 0%; }
            100% { background-position: 200% 0%; }
        }
        .sparkle-burst {
            position: absolute;
            pointer-events: none;
        }
        .sparkle {
            position: absolute;
            width: 8px; height: 8px;
            background: #ffd700;
            clip-path: polygon(50% 0%, 61% 35%, 98% 35%, 68% 57%, 79% 91%, 50% 70%, 21% 91%, 32% 57%, 2% 35%, 39% 35%);
            animation: sparkleAnim 1s ease-out forwards;
        }
        @keyframes sparkleAnim {
            0% { opacity: 1; transform: translate(0, 0) scale(0) rotate(0deg); }
            100% { opacity: 0; transform: translate(var(--tx), var(--ty)) scale(1.5) rotate(360deg); }
        }
        .floating-hearts {
            position: fixed;
            top: 0; left: 0;
            width: 100%; height: 100%;
            pointer-events: none;
            z-index: 5;
            overflow: hidden;
        }
        .heart-float {
            position: absolute;
            font-size: 20px;
            animation: heartFloat 6s ease-in-out infinite;
            opacity: 0;
        }
        @keyframes heartFloat {
            0% { transform: translateY(100vh) rotate(0deg) scale(0); opacity: 0; }
            10% { opacity: 0.8; }
            90% { opacity: 0.8; }
            100% { transform: translateY(-100vh) rotate(360deg) scale(1.5); opacity: 0; }
        }
        .answered-count {
            text-align: center;
            font-size: 1.2rem;
            color: #ffd700;
            margin-bottom: 30px;
            font-family: 'Great Vibes', cursive;
            font-size: 2rem;
        }
        @media (max-width: 768px) {
            .intro-title { font-size: 2.2rem; }
            .final-text { font-size: 2.5rem; }
            .question-card { padding: 25px; }
            .btn { padding: 15px 40px; font-size: 1.1rem; }
            .fairy { width: 80px; height: 100px; }
            .question-text { font-size: 1.1rem; }
            .stamp-pad { width: 160px; height: 160px; }
        }
    </style>
</head>
<body>
    <div class="progress-container">
        <div class="progress-bar" id="progressBar"></div>
    </div>

    <div class="bg-container">
        <img src="IMG_0696.png" alt="Dreamy Garden" class="bg-image">
    </div>
    <div class="bg-overlay"></div>

    <div class="particles" id="particles"></div>
    <div class="floating-hearts" id="floatingHearts"></div>
    <div class="fairy-container" id="fairyContainer"></div>

    <div class="container">
        <div class="intro-section" id="introSection">
            <div class="intro-heart">💌</div>
            <h1 class="intro-title">A Little Pact Between<br>Saye-e-Dil and Rana Bilal Naveed</h1>
            <p class="tiny-note">A Tiny Note (Do not Take It Too Serious)</p>
            <p class="intro-subtitle">Please answer honestly, okay?</p>
            <p class="warning-text">I wrote really long code for this bilal sahab do not ignore and answer nicely otherwise get ready</p>
            <div class="scroll-hint">Scroll to begin</div>
        </div>

        <div class="question-section" id="questionSection">
            <h2 class="section-title">Answer Me This</h2>
            <div class="answered-count" id="answeredCount">0 / 18 answered</div>

            <div class="question-card" data-index="0">
                <div class="question-icon">🦋</div>
                <div class="question-number">Question #1</div>
                <div class="question-text">
                    Will you promise that you will never call another girl <span class="highlight">"Saye-e-Dil"</span>?<br><br>
                    Because there is only one Saye-e-Dil in this world… and that is me
                </div>
                <div class="button-container">
                    <button class="btn btn-yes" onclick="answerYes(this, 0)">Yes</button>
                    <button class="btn btn-no" id="noBtn0" onclick="answerNo(this, 0)">No</button>
                </div>
            </div>

            <div class="question-card" data-index="1">
                <div class="question-icon">🌷</div>
                <div class="question-number">Question #2</div>
                <div class="question-text">
                    If we ever stop talking… like for 3 days… will you send me a song that says everything you cannot say in words?<br><br>
                    Because I know you struggle to say it directly
                </div>
                <div class="button-container">
                    <button class="btn btn-yes" onclick="answerYes(this, 1)">Yes</button>
                    <button class="btn btn-no" id="noBtn1" onclick="answerNo(this, 1)">No</button>
                </div>
            </div>

            <div class="question-card" data-index="2">
                <div class="question-icon">💌</div>
                <div class="question-number">Question #3</div>
                <div class="question-text">
                    You will talk to me a lot, right?<br><br>
                    Like your day, your thoughts, your stress, your happiness… even the tiny things?<br><br>
                    And do not worry, your secrets will always be safe with me
                </div>
                <div class="button-container">
                    <button class="btn btn-yes" onclick="answerYes(this, 2)">Yes</button>
                    <button class="btn btn-no" id="noBtn2" onclick="answerNo(this, 2)">No</button>
                </div>
            </div>

            <div class="question-card" data-index="3">
                <div class="question-icon">🌸</div>
                <div class="question-number">Question #4</div>
                <div class="question-text">
                    If we ever have an argument… will you be the one who comes first to fix it with me?
                </div>
                <div class="button-container">
                    <button class="btn btn-yes" onclick="answerYes(this, 3)">Yes</button>
                    <button class="btn btn-no" id="noBtn3" onclick="answerNo(this, 3)">No</button>
                </div>
            </div>

            <div class="question-card" data-index="4">
                <div class="question-icon">📸</div>
                <div class="question-number">Question #5</div>
                <div class="question-text">
                    Whenever you take a picture… I get to see it first, right?<br><br>
                    Before anyone else… even before posting?
                </div>
                <div class="button-container">
                    <button class="btn btn-yes" onclick="answerYes(this, 4)">Yes</button>
                    <button class="btn btn-no" id="noBtn4" onclick="answerNo(this, 4)">No</button>
                </div>
            </div>

            <div class="question-card" data-index="5">
                <div class="question-icon">🌙</div>
                <div class="question-number">Question #6</div>
                <div class="question-text">
                    If I say <span class="highlight">"I am fine"</span> but I am clearly not fine… will you keep asking until I tell you the truth?
                </div>
                <div class="button-container">
                    <button class="btn btn-yes" onclick="answerYes(this, 5)">Yes</button>
                    <button class="btn btn-no" id="noBtn5" onclick="answerNo(this, 5)">No</button>
                </div>
            </div>

            <div class="question-card" data-index="6">
                <div class="question-icon">🐣</div>
                <div class="question-number">Question #7</div>
                <div class="question-text">
                    If I randomly miss you at 2 AM… will you not judge me the next morning?
                </div>
                <div class="button-container">
                    <button class="btn btn-yes" onclick="answerYes(this, 6)">Yes</button>
                    <button class="btn btn-no" id="noBtn6" onclick="answerNo(this, 6)">No</button>
                </div>
            </div>

            <div class="question-card" data-index="7">
                <div class="question-icon">🍓</div>
                <div class="question-number">Question #8</div>
                <div class="question-text">
                    If someone asks who your favorite person is… will you at least think of me first?
                </div>
                <div class="button-container">
                    <button class="btn btn-yes" onclick="answerYes(this, 7)">Yes</button>
                    <button class="btn btn-no" id="noBtn7" onclick="answerNo(this, 7)">No</button>
                </div>
            </div>

            <div class="question-card" data-index="8">
                <div class="question-icon">🎧</div>
                <div class="question-number">Question #9</div>
                <div class="question-text">
                    If a song or reel reminds you of me… will you send it instantly without hesitation?
                </div>
                <div class="button-container">
                    <button class="btn btn-yes" onclick="answerYes(this, 8)">Yes</button>
                    <button class="btn btn-no" id="noBtn8" onclick="answerNo(this, 8)">No</button>
                </div>
            </div>

            <div class="question-card" data-index="9">
                <div class="question-icon">💬</div>
                <div class="question-number">Question #10</div>
                <div class="question-text">
                    If I ever text too much… will you still reply nicely and not get annoyed?
                </div>
                <div class="button-container">
                    <button class="btn btn-yes" onclick="answerYes(this, 9)">Yes</button>
                    <button class="btn btn-no" id="noBtn9" onclick="answerNo(this, 9)">No</button>
                </div>
            </div>

            <div class="question-card" data-index="10">
                <div class="question-icon">🙃</div>
                <div class="question-number">Question #11</div>
                <div class="question-text">
                    Will you stop replying with <span class="highlight">"acha hmm ok"</span>?<br><br>
                    Because I never know what to reply back and then I think ke ap mere se tung agaye ho?
                </div>
                <div class="button-container">
                    <button class="btn btn-yes" onclick="answerYes(this, 10)">Yes</button>
                    <button class="btn btn-no" id="noBtn10" onclick="answerNo(this, 10)">No</button>
                </div>
            </div>

            <div class="question-card" data-index="11">
                <div class="question-icon">⏰</div>
                <div class="question-number">Question #12</div>
                <div class="question-text">
                    Will you text me every day at 10 pm… even if you are busy… even after arguments… like your daily responsibility? <span class="highlight">Because I am your responsibility</span>
                </div>
                <div class="button-container">
                    <button class="btn btn-yes" onclick="answerYes(this, 11)">Yes</button>
                    <button class="btn btn-no" id="noBtn11" onclick="answerNo(this, 11)">No</button>
                </div>
            </div>

            <div class="question-card" data-index="12">
                <div class="question-icon">🤍</div>
                <div class="question-number">Question #13</div>
                <div class="question-text">
                    If I ever say something hurtful without meaning it… will you not take it to your heart?<br><br>
                    Just forgive me thinking <span class="highlight">"ye tou Pagal hai kuch bi bol deti hai aur kr deti hai krne se Pehle sochti ni"</span>
                </div>
                <div class="button-container">
                    <button class="btn btn-yes" onclick="answerYes(this, 12)">Yes</button>
                    <button class="btn btn-no" id="noBtn12" onclick="answerNo(this, 12)">No</button>
                </div>
            </div>

            <div class="question-card" data-index="13">
                <div class="question-icon">😂</div>
                <div class="question-number">Question #14</div>
                <div class="question-text">
                    Will you be funny with me?<br><br>
                    Because I like a funny, chill person… otherwise vibe off ho jati hai
                </div>
                <div class="button-container">
                    <button class="btn btn-yes" onclick="answerYes(this, 13)">Yes</button>
                    <button class="btn btn-no" id="noBtn13" onclick="answerNo(this, 13)">No</button>
                </div>
            </div>

            <div class="question-card" data-index="14">
                <div class="question-icon">🧥</div>
                <div class="question-number">Question #15</div>
                <div class="question-text">
                    If we meet in winters… will you give me your old jacket?<br><br>
                    So I can keep it like a memory of you… just in case one day you stop talking to me. Aur decide kr lo ke ab kabhi jahanara se bat ni krni. <span class="highlight">Phir ma wo jacket rakh kr samjungi ke bilal hai</span>
                </div>
                <div class="button-container">
                    <button class="btn btn-yes" onclick="answerYes(this, 14)">Yes</button>
                    <button class="btn btn-no" id="noBtn14" onclick="answerNo(this, 14)">No</button>
                </div>
            </div>

            <div class="question-card" data-index="15">
                <div class="question-icon">💭</div>
                <div class="question-number">Question #16</div>
                <div class="question-text">
                    Will you always listen to me properly?<br><br>
                    Because I talk a lot… and if someone ignores me I just go quiet and sad
                </div>
                <div class="button-container">
                    <button class="btn btn-yes" onclick="answerYes(this, 15)">Yes</button>
                    <button class="btn btn-no" id="noBtn15" onclick="answerNo(this, 15)">No</button>
                </div>
            </div>

            <div class="question-card" data-index="16">
                <div class="question-icon">🫶</div>
                <div class="question-number">Question #17</div>
                <div class="question-text">
                    If I suddenly go quiet and stop yapping… will you notice?<br><br>
                    Like <span class="highlight">"what happened to her… why is she so silent?"</span>
                </div>
                <div class="button-container">
                    <button class="btn btn-yes" onclick="answerYes(this, 16)">Yes</button>
                    <button class="btn btn-no" id="noBtn16" onclick="answerNo(this, 16)">No</button>
                </div>
            </div>

            <div class="question-card" data-index="17">
                <div class="question-icon">💖</div>
                <div class="question-number">Question #18</div>
                <div class="question-text">
                    Will you never take my affection and care for granted? And not show me attitude or ego?<br><br>
                    And always value it… even the small things I do for you?
                </div>
                <div class="button-container">
                    <button class="btn btn-yes" onclick="answerYes(this, 17)">Yes</button>
                    <button class="btn btn-no" id="noBtn17" onclick="answerNo(this, 17)">No</button>
                </div>
            </div>
        </div>

        <div class="final-section" id="finalSection">
            <div class="final-heart">🤍</div>
            <h2 class="final-text">I Accept This Peace Pact</h2>
            <p class="final-subtext">Forever and always, insha Allah</p>
            
            <div class="thumb-stamp-section" id="thumbStampSection">
                <div class="stamp-pad" id="stampPad" onclick="doThumbStamp()">
                    <div class="thumb-print" id="thumbPrint"></div>
                    <span class="stamp-pad-text">Stamp Here</span>
                </div>
                <p class="stamp-instruction">Put your thumb here to seal the pact</p>
                <div class="disturb-text" id="disturbText">So now I can disturb you!</div>
                <div class="cute-fairy-final" id="cuteFairyFinal">🧚‍♀️💕</div>
            </div>
        </div>
    </div>

    <script>
        let answeredItems = new Array(18).fill(false);
        let currentQuestion = 0;
        let stampDone = false;
        const questionCards = document.querySelectorAll('.question-card');
        const progressBar = document.getElementById('progressBar');
        const answeredCount = document.getElementById('answeredCount');
        const finalSection = document.getElementById('finalSection');
        const floatingHearts = document.getElementById('floatingHearts');
        const fairyContainer = document.getElementById('fairyContainer');
        const questionSection = document.getElementById('questionSection');
        const thumbStampSection = document.getElementById('thumbStampSection');
        const disturbText = document.getElementById('disturbText');
        const cuteFairyFinal = document.getElementById('cuteFairyFinal');

        const fairyActions = [
            { gift: '🦋', color: '#ffd700', action: 'releases a butterfly' },
            { gift: '🌷', color: '#ff69b4', action: 'gives a rose' },
            { gift: '💌', color: '#ff1493', action: 'gives a love letter' },
            { gift: '🌸', color: '#ffb6c1', action: 'scatters flower petals' },
            { gift: '📸', color: '#ffd700', action: 'captures a magical photo' },
            { gift: '🌙', color: '#e6e6fa', action: 'brings moonlight glow' },
            { gift: '🐣', color: '#ffd700', action: 'gives a warm hug' },
            { gift: '🍓', color: '#ff4757', action: 'offers sweet strawberries' },
            { gift: '🎧', color: '#7bed9f', action: 'plays a love song' },
            { gift: '💬', color: '#70a1ff', action: 'sends a sweet message' },
            { gift: '🙃', color: '#ffa502', action: 'does a funny dance' },
            { gift: '⏰', color: '#ff6348', action: 'sets a love alarm' },
            { gift: '🤍', color: '#ffffff', action: 'gives a pure heart' },
            { gift: '😂', color: '#ffeaa7', action: 'tells a funny joke' },
            { gift: '🧥', color: '#dfe6e9', action: 'wraps in warm comfort' },
            { gift: '💭', color: '#a29bfe', action: 'whispers sweet thoughts' },
            { gift: '🫶', color: '#fd79a8', action: 'shows caring hands' },
            { gift: '💖', color: '#ff6b81', action: 'gives endless love' }
        ];

        const laughMessages = [
            "Hehe you had no choice!",
            "Caught you!",
            "Too late to run!",
            "You are mine now!",
            "No escaping!",
            "Gotcha!",
            "Trapped in love!",
            "No way out!",
            "You are stuck with me!",
            "Haha nice try!",
            "Fairy says no escape!",
            "Love wins!",
            "Too cute to resist!",
            "You are caught!",
            "No running from love!",
            "Fairy magic!",
            "You are trapped!",
            "Forever and ever!"
        ];

        function init() {
            questionCards.forEach((card, i) => {
                card.style.display = 'none';
                card.classList.remove('active');
            });
            questionCards[0].style.display = 'block';
            questionCards[0].classList.add('active');
        }

        function createParticles() {
            const container = document.getElementById('particles');
            for (let i = 0; i < 60; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.animationDelay = Math.random() * 20 + 's';
                particle.style.animationDuration = (15 + Math.random() * 10) + 's';
                container.appendChild(particle);
            }
        }

        function createFireflies() {
            const container = document.getElementById('particles');
            for (let i = 0; i < 15; i++) {
                const firefly = document.createElement('div');
                firefly.className = 'firefly';
                firefly.style.left = Math.random() * 100 + '%';
                firefly.style.top = Math.random() * 100 + '%';
                firefly.style.animationDelay = Math.random() * 8 + 's';
                container.appendChild(firefly);
            }
        }

        function createFloatingHeart() {
            const heart = document.createElement('div');
            heart.className = 'heart-float';
            const hearts = ['🤍', '💛', '✨', '🌟', '💫'];
            heart.innerHTML = hearts[Math.floor(Math.random() * hearts.length)];
            heart.style.left = Math.random() * 100 + '%';
            heart.style.animationDuration = (5 + Math.random() * 4) + 's';
            heart.style.fontSize = (15 + Math.random() * 25) + 'px';
            floatingHearts.appendChild(heart);
            setTimeout(() => heart.remove(), 8000);
        }

        function createSparkleBurst(element) {
            const rect = element.getBoundingClientRect();
            const burst = document.createElement('div');
            burst.className = 'sparkle-burst';
            burst.style.left = (rect.left + rect.width / 2) + 'px';
            burst.style.top = (rect.top + rect.height / 2) + 'px';
            document.body.appendChild(burst);
            for (let i = 0; i < 12; i++) {
                const sparkle = document.createElement('div');
                sparkle.className = 'sparkle';
                const angle = (i / 12) * Math.PI * 2;
                const distance = 50 + Math.random() * 50;
                sparkle.style.setProperty('--tx', Math.cos(angle) * distance + 'px');
                sparkle.style.setProperty('--ty', Math.sin(angle) * distance + 'px');
                burst.appendChild(sparkle);
            }
            setTimeout(() => burst.remove(), 1000);
        }

        function createFairyLaugh(x, y, message) {
            const laugh = document.createElement('div');
            laugh.className = 'fairy-laugh';
            laugh.innerHTML = message;
            laugh.style.left = x + 'px';
            laugh.style.top = y + 'px';
            document.body.appendChild(laugh);
            requestAnimationFrame(() => { laugh.classList.add('show'); });
            setTimeout(() => laugh.remove(), 2500);
        }

        function createFairy(index, x, y) {
            const action = fairyActions[index];
            const fairy = document.createElement('div');
            fairy.className = 'fairy fairy-appear';
            fairy.style.left = x + 'px';
            fairy.style.top = y + 'px';
            fairy.innerHTML = `
                <svg viewBox="0 0 100 120" xmlns="http://www.w3.org/2000/svg">
                    <ellipse cx="25" cy="40" rx="20" ry="30" fill="${action.color}" opacity="0.6" transform="rotate(-20 25 40)"/>
                    <ellipse cx="75" cy="40" rx="20" ry="30" fill="${action.color}" opacity="0.6" transform="rotate(20 75 40)"/>
                    <ellipse cx="20" cy="50" rx="15" ry="25" fill="${action.color}" opacity="0.4" transform="rotate(-30 20 50)"/>
                    <ellipse cx="80" cy="50" rx="15" ry="25" fill="${action.color}" opacity="0.4" transform="rotate(30 80 50)"/>
                    <ellipse cx="50" cy="60" rx="15" ry="25" fill="url(#soulGradient)"/>
                    <circle cx="50" cy="30" r="18" fill="url(#soulGradient)"/>
                    <circle cx="44" cy="28" r="3" fill="#fff"/>
                    <circle cx="56" cy="28" r="3" fill="#fff"/>
                    <circle cx="44" cy="28" r="1.5" fill="#1a1a2e"/>
                    <circle cx="56" cy="28" r="1.5" fill="#1a1a2e"/>
                    <path d="M 45 35 Q 50 38 55 35" stroke="#1a1a2e" stroke-width="1.5" fill="none"/>
                    <path d="M 32 25 Q 50 10 68 25" stroke="${action.color}" stroke-width="3" fill="none"/>
                    <path d="M 35 20 Q 50 5 65 20" stroke="${action.color}" stroke-width="2" fill="none"/>
                    <circle cx="50" cy="8" r="8" fill="none" stroke="#ffd700" stroke-width="2" opacity="0.8"/>
                    <circle cx="50" cy="8" r="5" fill="#ffd700" opacity="0.5"/>
                    <path d="M 38 50 Q 30 60 25 55" stroke="url(#soulGradient)" stroke-width="3" fill="none" stroke-linecap="round"/>
                    <path d="M 62 50 Q 70 60 75 55" stroke="url(#soulGradient)" stroke-width="3" fill="none" stroke-linecap="round"/>
                    <text x="65" y="55" font-size="20" text-anchor="middle">${action.gift}</text>
                    <circle cx="20" cy="20" r="2" fill="#ffd700" opacity="0.8">
                        <animate attributeName="opacity" values="0.8;0.2;0.8" dur="1s" repeatCount="indefinite"/>
                    </circle>
                    <circle cx="80" cy="25" r="2" fill="#ffd700" opacity="0.6">
                        <animate attributeName="opacity" values="0.6;0.1;0.6" dur="1.2s" repeatCount="indefinite"/>
                    </circle>
                    <circle cx="50" cy="10" r="1.5" fill="#ff69b4" opacity="0.7">
                        <animate attributeName="opacity" values="0.7;0.2;0.7" dur="0.8s" repeatCount="indefinite"/>
                    </circle>
                </svg>
            `;
            fairyContainer.appendChild(fairy);
            setTimeout(() => {
                const gift = document.createElement('div');
                gift.className = 'fairy-gift';
                gift.innerHTML = action.gift;
                gift.style.left = (x + 50) + 'px';
                gift.style.top = (y + 20) + 'px';
                gift.style.color = action.color;
                fairyContainer.appendChild(gift);
                setTimeout(() => gift.remove(), 3000);
            }, 1000);
            for (let i = 0; i < 8; i++) {
                setTimeout(() => {
                    const dust = document.createElement('div');
                    dust.className = 'fairy-dust';
                    dust.style.left = (x + 50 + (Math.random() - 0.5) * 60) + 'px';
                    dust.style.top = (y + 60 + (Math.random() - 0.5) * 60) + 'px';
                    dust.style.setProperty('--dx', (Math.random() - 0.5) * 100 + 'px');
                    dust.style.setProperty('--dy', (Math.random() - 0.5) * 100 + 'px');
                    fairyContainer.appendChild(dust);
                    setTimeout(() => dust.remove(), 2000);
                }, i * 200);
            }
            setTimeout(() => fairy.remove(), 4000);
        }

        function showNextQuestion(currentIndex) {
            questionCards[currentIndex].style.display = 'none';
            questionCards[currentIndex].classList.remove('active');
            if (currentIndex + 1 < questionCards.length) {
                questionCards[currentIndex + 1].style.display = 'block';
                questionCards[currentIndex + 1].classList.add('active');
                questionSection.scrollIntoView({ behavior: 'smooth', block: 'start' });
            } else {
                finalSection.classList.add('visible');
                finalSection.scrollIntoView({ behavior: 'smooth', block: 'center' });
                for (let i = 0; i < 30; i++) { setTimeout(createFloatingHeart, i * 150); }
                setTimeout(() => { thumbStampSection.classList.add('visible'); }, 2000);
            }
        }

        function answerYes(btn, index) {
            if (index !== currentQuestion) { shakeElement(btn); return; }
            answeredItems[index] = true;
            questionCards[index].classList.add('answered');
            const btnContainer = btn.parentElement;
            btnContainer.innerHTML = '<span style="color: #ffd700; font-size: 1.3rem; font-weight: 600;">You had no choice</span>';
            createSparkleBurst(btn);
            const rect = btn.getBoundingClientRect();
            const fairyX = rect.left + rect.width / 2 - 60;
            const fairyY = rect.top - 120;
            createFairy(index, fairyX, fairyY);
            createFairyLaugh(rect.left + rect.width / 2, rect.top - 50, laughMessages[index]);
            for (let i = 0; i < 8; i++) { setTimeout(createFloatingHeart, i * 100); }
            updateProgress();
            setTimeout(() => { showNextQuestion(index); currentQuestion++; }, 2500);
        }

        function answerNo(btn, index) {
            const card = btn.closest('.question-card');
            const cardRect = card.getBoundingClientRect();
            const maxX = cardRect.width - btn.offsetWidth - 30;
            const maxY = cardRect.height - btn.offsetHeight - 30;
            const randomX = 15 + Math.random() * maxX;
            const randomY = 15 + Math.random() * maxY;
            btn.classList.add('running');
            btn.style.left = randomX + 'px';
            btn.style.top = randomY + 'px';
            btn.style.animation = 'shake 0.3s ease';
            setTimeout(() => btn.style.animation = '', 300);
        }

        function updateProgress() {
            const answered = answeredItems.filter(x => x).length;
            const progress = (answered / answeredItems.length) * 100;
            progressBar.style.width = progress + '%';
            answeredCount.textContent = answered + ' / 18 answered';
        }

        function shakeElement(element) {
            element.style.animation = 'shake 0.5s ease';
            setTimeout(() => element.style.animation = '', 500);
        }

        const style = document.createElement('style');
        style.textContent = `
            @keyframes shake {
                0%, 100% { transform: translateX(0); }
                20% { transform: translateX(-10px); }
                40% { transform: translateX(10px); }
                60% { transform: translateX(-5px); }
                80% { transform: translateX(5px); }
            }
        `;
        document.head.appendChild(style);

        let isScrolling = false;
        window.addEventListener('scroll', () => {
            if (isScrolling) return;
            const activeCard = document.querySelector('.question-card.active');
            if (activeCard && !answeredItems[currentQuestion]) {
                const rect = activeCard.getBoundingClientRect();
                if (rect.bottom < 0 || rect.top > window.innerHeight) {
                    isScrolling = true;
                    activeCard.scrollIntoView({ behavior: 'smooth', block: 'center' });
                    setTimeout(() => isScrolling = false, 500);
                }
            }
        });

        function doThumbStamp() {
            if (stampDone) return;
            stampDone = true;
            const thumbPrint = document.getElementById('thumbPrint');
            const stampPad = document.getElementById('stampPad');
            const stampText = stampPad.querySelector('.stamp-pad-text');
            thumbPrint.classList.add('stamped');
            stampText.style.opacity = '0';
            stampPad.style.transform = 'scale(1.1)';
            setTimeout(() => { stampPad.style.transform = 'scale(1)'; }, 200);
            for (let i = 0; i < 20; i++) { setTimeout(createFloatingHeart, i * 100); }
            createSparkleBurst(stampPad);
            setTimeout(() => { disturbText.classList.add('show'); }, 800);
            setTimeout(() => { cuteFairyFinal.classList.add('show'); }, 1500);
            setTimeout(() => {
                createFairyLaugh(window.innerWidth / 2 - 100, window.innerHeight / 2 + 100, "Hehe pact sealed!");
            }, 2000);
        }

        createParticles();
        createFireflies();
        setInterval(createFloatingHeart, 1500);
        init();

        document.addEventListener('mousemove', (e) => {
            const bg = document.querySelector('.bg-image');
            const x = (window.innerWidth - e.pageX) / 100;
            const y = (window.innerHeight - e.pageY) / 100;
            bg.style.transform = `scale(1.05) translate(${x}px, ${y}px)`;
        });
    </script>
</body>
</html>'''

with open('/mnt/agents/output/little_pact.html', 'w', encoding='utf-8') as f:
    f.write(html_content)

print("Full code saved successfully!")
print(f"Total file size: {len(html_content)} characters")
