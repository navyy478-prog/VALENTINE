#HAPPY 4 MONTHS ANNIVERSARY 🥹🫠
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Infinity Love | Teena ❤️</title>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Montserrat:wght@300;400;600;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --pink: #ff3366;
            --purple: #7000ff;
            --glass: rgba(255, 255, 255, 0.08);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; touch-action: none; -webkit-tap-highlight-color: transparent; }
        
        body {
            background: #050505;
            color: white;
            font-family: 'Montserrat', sans-serif;
            overflow: hidden;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        /* Background Elements */
        #bg-canvas, #fw-canvas { position: fixed; top: 0; left: 0; width: 100%; height: 100%; z-index: -1; }
        #fw-canvas { z-index: 100; pointer-events: none; }

        .container {
            width: 92%; max-width: 450px;
            background: var(--glass);
            backdrop-filter: blur(20px);
            border-radius: 40px; padding: 40px 25px;
            text-align: center; display: none;
            border: 1px solid rgba(255,255,255,0.1);
            box-shadow: 0 25px 50px rgba(0,0,0,0.5);
            z-index: 10;
        }

        .active { display: block; animation: zoomIn 0.8s cubic-bezier(0.19, 1, 0.22, 1); }
        @keyframes zoomIn { from { opacity: 0; transform: scale(0.8) translateY(20px); } to { opacity: 1; transform: scale(1) translateY(0); } }

        h1 { font-family: 'Dancing Script', cursive; font-size: 3rem; color: var(--pink); text-shadow: 0 0 15px rgba(255,51,102,0.4); }
        p { font-weight: 300; font-size: 0.95rem; line-height: 1.6; margin: 15px 0; opacity: 0.8; }

        /* Timer Grid */
        .t-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 10px; margin: 20px 0; }
        .t-box { background: rgba(0,0,0,0.3); padding: 10px; border-radius: 15px; border: 1px solid rgba(255,51,102,0.2); }
        .t-num { display: block; font-size: 1.2rem; font-weight: 800; color: var(--pink); }
        .t-lbl { font-size: 0.6rem; text-transform: uppercase; opacity: 0.6; }

        /* Scratch Card */
        .sc-wrap { position: relative; width: 240px; height: 240px; margin: 20px auto; border-radius: 20px; overflow: hidden; border: 2px solid var(--pink); }
        .sc-res { position: absolute; top:0; left:0; width:100%; height:100%; background:#111; display:flex; flex-direction:column; align-items:center; justify-content:center; }
        #sc-canvas { position: absolute; top:0; left:0; z-index: 2; cursor: crosshair; }

        /* Buttons */
        .btn {
            background: white; color: black; border: none; padding: 18px 30px;
            border-radius: 100px; font-weight: 700; text-transform: uppercase;
            letter-spacing: 1px; cursor: pointer; width: 100%; transition: 0.3s;
            margin-top: 10px; box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }
        .btn:hover { background: var(--pink); color: white; transform: translateY(-3px); }

        .final-txt {
            position: fixed; top: 50%; left: 50%; transform: translate(-50%, -50%);
            font-family: 'Dancing Script', cursive; font-size: 4.5rem;
            text-align: center; z-index: 101; display: none; text-shadow: 0 0 30px var(--pink);
        }
    </style>
</head>
<body>

    <canvas id="bg-canvas"></canvas>
    <canvas id="fw-canvas"></canvas>
    <audio id="bgm" loop src="https://www.bensound.com/bensound-music/bensound-love.mp3"></audio>

    <div id="p1" class="container active">
        <h1>For You, Teena</h1>
        <p>A journey that started 4 months ago...</p>
        <div class="t-grid">
            <div class="t-box"><span class="t-num" id="td-d">00</span><span class="t-lbl">Days</span></div>
            <div class="t-box"><span class="t-num" id="td-h">00</span><span class="t-lbl">Hrs</span></div>
            <div class="t-box"><span class="t-num" id="td-m">00</span><span class="t-lbl">Min</span></div>
            <div class="t-box" style="grid-column: span 3;"><span class="t-num" id="td-s">00</span><span class="t-lbl">Seconds of Togetherness</span></div>
        </div>
        <button class="btn" onclick="startApp(2)">Open Memories 💌</button>
    </div>

    <div id="p2" class="container">
        <h1>My Feelings</h1>
        <p style="font-style: italic; font-size: 1.1rem;">
            "Aapki hansi meri kamzori hai,<br>
            Aapka saath meri zaruri hai.<br>
            4 mahine toh bas ek shuruat hai,<br>
            Humein bitani poori zindagi saath hai."
        </p>
        <button class="btn" onclick="next(3)">Next Secret ✨</button>
    </div>

    <div id="p3" class="container">
        <h1>Love Test 🧩</h1>
        <p>How much do you love Navuu?</p>
        <button class="btn" style="background: rgba(255,255,255,0.1); color: white; margin-bottom: 10px;" onclick="alert('Thoda sa? Galat jawab! 😜')">Thoda sa 🤏</button>
        <button class="btn" style="background: rgba(255,255,255,0.1); color: white; margin-bottom: 10px;" onclick="alert('Bohot saara? Thoda aur socho.. ✨')">Bohot saara! ✨</button>
        <button class="btn" onclick="next(4)">Infinite / Jaan se zyada ❤️</button>
    </div>

    <div id="p4" class="container">
        <h1>Scratch the Card</h1>
        <p>Reveal what's in my heart...</p>
        <div class="sc-wrap">
            <div class="sc-res">
                <span style="font-size: 3rem;">💍</span>
                <p style="color:var(--pink); font-weight:800;">YOU ARE MINE!</p>
            </div>
            <canvas id="sc-canvas" width="240" height="240"></canvas>
        </div>
        <button id="sc-btn" class="btn" style="display:none;" onclick="next(5)">Go Ahead 🚀</button>
    </div>

    <div id="p5" class="container">
        <h1>The Vow 💍</h1>
        <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExM3h0Y2N4YnI3ZHR4Z285eDR0Z285eDR0Z285eDR0Z285eDR0ZyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/Lp71UqhcHh46OKH39W/giphy.gif" style="width:100%; border-radius: 20px;">
        <p>Will you stay by my side in every up and down of life?</p>
        <button class="btn" onclick="next(6)">Yes, Forever 😍</button>
    </div>

    <div id="p6" class="container">
        <h1>Final Note 🔐</h1>
        <div style="text-align: left; background: rgba(0,0,0,0.2); padding: 20px; border-radius: 20px; font-size: 0.85rem;">
            <p>Dear Teena,</p><br>
            <p>In 4 mahino mein aapne meri duniya badal di. Thank you for being my peace. I promise to love you more with every passing second.</p>
            <p style="text-align: right; font-family: 'Dancing Script'; font-size: 1.5rem; color: var(--pink);">- Ur Navuu</p>
        </div>
        <button class="btn" style="background: var(--pink); color: white;" onclick="triggerSkyShot()">Launch Sky Shot 🎇</button>
    </div>

    <div id="f-text" class="final-txt">I LOVE YOU <br> TEENA ❤️</div>

    <script>
        // --- Timer Logic ---
        const start = new Date(2025, 9, 24); // Year, Month(0-11), Day
        function updateTimer() {
            const diff = new Date() - start;
            document.getElementById('td-d').innerText = Math.floor(diff/86400000);
            document.getElementById('td-h').innerText = Math.floor((diff/3600000)%24);
            document.getElementById('td-m').innerText = Math.floor((diff/60000)%60);
            document.getElementById('td-s').innerText = Math.floor((diff/1000)%60);
        }
        setInterval(updateTimer, 1000);

        // --- Background Particles ---
        const bCan = document.getElementById('bg-canvas');
        const bCtx = bCan.getContext('2d');
        bCan.width = window.innerWidth; bCan.height = window.innerHeight;
        let pts = [];
        for(let i=0; i<60; i++) pts.push({x:Math.random()*bCan.width, y:Math.random()*bCan.height, r:Math.random()*2, vx:Math.random()-0.5, vy:Math.random()-0.5});
        function drawBg() {
            bCtx.clearRect(0,0,bCan.width, bCan.height);
            bCtx.fillStyle = "rgba(255,51,102,0.3)";
            pts.forEach(p => {
                p.x+=p.vx; p.y+=p.vy;
                if(p.x<0||p.x>bCan.width) p.vx*=-1; if(p.y<0||p.y>bCan.height) p.vy*=-1;
                bCtx.beginPath(); bCtx.arc(p.x, p.y, p.r, 0, 6.28); bCtx.fill();
            });
            requestAnimationFrame(drawBg);
        }
        drawBg();

        // --- Scratch Logic ---
        const sc = document.getElementById('sc-canvas');
        const sCtx = sc.getContext('2d');
        let mDown = false;
        function initSC() {
            sCtx.fillStyle = '#555'; sCtx.fillRect(0,0,240,240);
            sCtx.fillStyle = '#fff'; sCtx.font = '18px Montserrat'; sCtx.textAlign='center'; sCtx.fillText('SCRATCH ME ❤️', 120, 125);
            sCtx.globalCompositeOperation = 'destination-out';
        }
        function doScratch(e) {
            if(!mDown) return;
            const r = sc.getBoundingClientRect();
            const x = (e.clientX || e.touches[0].clientX) - r.left;
            const y = (e.clientY || e.touches[0].clientY) - r.top;
            sCtx.beginPath(); sCtx.arc(x, y, 30, 0, 6.28); sCtx.fill();
            let d = sCtx.getImageData(0,0,240,240).data, c=0;
            for(let i=3; i<d.length; i+=4) if(d[i]===0) c++;
            if(c > 240*240*0.6) document.getElementById('sc-btn').style.display='block';
        }
        sc.addEventListener('mousedown', ()=>mDown=true); sc.addEventListener('touchstart', ()=>mDown=true);
        window.addEventListener('mouseup', ()=>mDown=false); window.addEventListener('touchend', ()=>mDown=false);
        sc.addEventListener('mousemove', doScratch); sc.addEventListener('touchmove', doScratch);
        initSC();

        // --- Sky Shot Logic ---
        const fCan = document.getElementById('fw-canvas');
        const fCtx = fCan.getContext('2d');
        fCan.width = window.innerWidth; fCan.height = window.innerHeight;
        function triggerSkyShot() {
            document.querySelectorAll('.container').forEach(c=>c.style.display='none');
            document.getElementById('f-text').style.display='block';
            setInterval(()=>{
                const x = Math.random()*fCan.width, y = Math.random()*fCan.height/2;
                const col = `hsl(${Math.random()*360}, 100%, 60%)`;
                let p = []; for(let i=0; i<30; i++) p.push({x,y,vx:Math.random()*4-2, vy:Math.random()*4-2, a:1});
                function ani() {
                    fCtx.fillStyle = 'rgba(5,5,5,0.1)'; fCtx.fillRect(0,0,fCan.width, fCan.height);
                    p.forEach((pt, i)=>{
                        pt.x+=pt.vx; pt.y+=pt.vy; pt.vy+=0.02; pt.a-=0.01;
                        fCtx.globalAlpha = pt.a; fCtx.fillStyle = col;
                        fCtx.beginPath(); fCtx.arc(pt.x, pt.y, 2, 0, 6.28); fCtx.fill();
                        if(pt.a<=0) p.splice(i,1);
                    });
                    if(p.length>0) requestAnimationFrame(ani);
                }
                ani();
            }, 500);
        }

        function startApp(n) { document.getElementById('bgm').play().catch(()=>{}); next(n); }
        function next(n) {
            document.querySelectorAll('.container').forEach(c => c.classList.remove('active'));
            document.getElementById('p' + n).classList.add('active');
        }
    </script>
</body>
</html>
