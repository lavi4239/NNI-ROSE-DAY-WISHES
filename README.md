# NNI-ROSE-DAY-WISHES
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rose Day Surprise</title>
    <style>
        :root {
            --rose-red: #e91e63;
            --soft-pink: #fce4ec;
            --dark-pink: #f06292;
        }

        body {
            margin: 0;
            padding: 0;
            background-color: var(--soft-pink);
            font-family: 'Arial Rounded MT Bold', 'Helvetica', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            overflow: hidden;
        }

        .phone-frame {
            width: 360px;
            height: 640px;
            background: #fff;
            border-radius: 40px;
            box-shadow: 0 25px 50px rgba(0,0,0,0.15);
            position: relative;
            overflow: hidden;
            border: 10px solid #333;
        }

        .screen {
            position: absolute;
            width: 100%;
            height: 100%;
            display: none;
            flex-direction: column;
            align-items: center;
            padding: 25px;
            box-sizing: border-box;
            background: #fff;
        }

        .active { display: flex; animation: slideUp 0.5s ease-out; }

        @keyframes slideUp {
            from { transform: translateY(30px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }

        /* Calendar Icon */
        .calendar {
            position: absolute;
            top: 25px;
            right: 25px;
            width: 65px;
            height: 70px;
            background: #fff;
            border: 2px solid #ddd;
            border-radius: 10px;
            text-align: center;
        }
        .cal-header { background: var(--rose-red); color: white; font-size: 10px; padding: 2px; border-radius: 8px 8px 0 0; }
        .cal-body { font-size: 24px; font-weight: bold; color: #333; }
        .cal-footer { font-size: 10px; color: var(--rose-red); font-weight: bold; }

        .bunny-icon { font-size: 85px; margin-top: 80px; }
        h1 { font-size: 26px; color: #333; margin: 30px 0 10px; text-align: center; }
        
        .btn {
            width: 85%;
            padding: 15px;
            margin: 10px 0;
            border: none;
            border-radius: 15px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
        }

        .btn-yes { background: var(--rose-red); color: white; }
        .btn-no { background: #fce4ec; color: #888; transition: 0.1s; }
        .btn-gift { background: var(--dark-pink); color: white; width: 160px; }

        /* Final Screen Special Layout */
        .bebbo-header { 
            font-size: 36px; 
            font-weight: 900; 
            color: var(--rose-red); 
            margin-top: 40px; 
            letter-spacing: 3px; 
        }

        .center-heart { 
            font-size: 110px; 
            margin: 30px 0; 
            animation: pulse 1.2s infinite; 
            color: var(--rose-red);
        }

        /* The Box where the QR code used to be */
        .nni-qr-box {
            width: 160px;
            height: 160px;
            border: 6px solid #333; /* Darker border like a QR frame */
            border-radius: 15px;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
            background-color: #fdfdfd;
        }

        .nni-text {
            font-size: 32px;
            font-weight: bold;
            color: #333;
            letter-spacing: 2px;
        }

        /* QR-like corner squares */
        .nni-qr-box::before {
            content: '';
            position: absolute;
            top: 10px; left: 10px;
            width: 30px; height: 30px;
            border: 4px solid #333;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.15); }
            100% { transform: scale(1); }
        }

        .letter {
            background: #fffafb;
            padding: 20px;
            border: 2px dashed var(--rose-red);
            border-radius: 15px;
            text-align: left;
            font-size: 14px;
            line-height: 1.6;
        }
    </style>
</head>
<body>

    <div class="phone-frame">
        
        <div id="p1" class="screen active">
            <div class="calendar">
                <div class="cal-header">FEB</div>
                <div class="cal-body">07</div>
                <div class="cal-footer">ROSE DAY</div>
            </div>
            <div class="bunny-icon">🌹🐰</div>
            <h1>Happy Rose Day!<br>Will you be my Valentine?</h1>
            <button class="btn btn-yes" onclick="showPage('p2')">YES OF COURSE</button>
            <button class="btn btn-no" id="noBtn" onmouseover="moveNoButton()">NO THANK YOU</button>
        </div>

        <div id="p2" class="screen">
            <h1 style="margin-top: 80px;">Yay, you said yes!</h1>
            <p>I made all these for you babe</p>
            <button class="btn btn-gift" onclick="showPage('p3')">Gift 1</button>
            <button class="btn btn-gift" onclick="showPage('p3')">Gift 2</button>
            <button class="btn btn-gift" onclick="showPage('p3')">Gift 3</button>
        </div>

        <div id="p3" class="screen">
            <h2>Your Rose Bouquet</h2>
            <div style="background:#fff; padding:10px; border-radius:15px; border:1px solid #ffb3c1; font-size:12px; margin:10px;">"You will forever be my only option"</div>
            <div style="font-size: 100px;">💐</div>
            <div style="background:#fff; padding:10px; border-radius:15px; border:1px solid #ffb3c1; font-size:12px; margin:10px;">"I can't imagine a life without you in it"</div>
            <button class="btn btn-yes" style="width: auto; padding: 10px 30px; margin-top:20px;" onclick="showPage('p4')">click me! ⮕</button>
        </div>

        <div id="p4" class="screen">
            <h2 style="color: var(--rose-red);">Words from my Heart</h2>
            <div class="letter">
                To the love of my life, you make my life so meaningful and I am so lucky to have you as my valentine this year. 
                I love you wholeheartedly and I can't wait to continue loving you for the rest of my life.
                <br><br><strong>Always, Forever ❤️</strong>
            </div>
            <button class="btn btn-yes" style="margin-top: 20px;" onclick="showPage('p5')">Next ⮕</button>
        </div>

        <div id="p5" class="screen">
            <div class="bebbo-header">BEBBO</div>
            
            <div class="center-heart">♥️</div>
            
            <div class="nni-qr-box">
                <div class="nni-text">NNI</div>
            </div>

            <p style="margin-top: 40px; font-size: 11px; color: #bbb; cursor: pointer;" onclick="location.reload()">click to restart!</p>
        </div>

    </div>

    <script>
        function showPage(id) {
            document.querySelectorAll('.screen').forEach(s => s.classList.remove('active'));
            document.getElementById(id).classList.add('active');
        }

        function moveNoButton() {
            const btn = document.getElementById('noBtn');
            const x = Math.random() * (window.innerWidth - btn.offsetWidth - 20);
            const y = Math.random() * (window.innerHeight - btn.offsetHeight - 20);
            btn.style.position = 'fixed';
            btn.style.left = x + 'px';
            btn.style.top = y + 'px';
        }
    </script>
</body>
</html>
