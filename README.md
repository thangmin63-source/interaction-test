# Interaction-test
Interaction-test 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Secure System</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
body {
    margin: 0;
        font-family: Arial, sans-serif;
            background: radial-gradient(circle, #1a002b, #000);
                color: white;
                    display: flex;
                        justify-content: center;
                            align-items: center;
                                height: 100vh;
                                    overflow: hidden;
                                    }

                                    .card {
                                        background: rgba(0,0,0,0.75);
                                            padding: 25px;
                                                border-radius: 15px;
                                                    text-align: center;
                                                        width: 320px;
                                                            box-shadow: 0 0 40px rgba(255,0,150,0.5);
                                                            }

                                                            .hidden { display: none; }

                                                            button {
                                                                padding: 10px 22px;
                                                                    margin: 10px;
                                                                        border: none;
                                                                            border-radius: 25px;
                                                                                font-size: 16px;
                                                                                    cursor: pointer;
                                                                                    }

                                                                                    .yes {
                                                                                        background: #ff4d8d;
                                                                                            color: white;
                                                                                            }

                                                                                            .no, .back {
                                                                                                background: #555;
                                                                                                    color: white;
                                                                                                        position: absolute;
                                                                                                        }

                                                                                                        .loader {
                                                                                                            border: 6px solid #333;
                                                                                                                border-top: 6px solid #ff4d8d;
                                                                                                                    border-radius: 50%;
                                                                                                                        width: 60px;
                                                                                                                            height: 60px;
                                                                                                                                animation: spin 1s linear infinite;
                                                                                                                                    margin: 20px auto;
                                                                                                                                    }

                                                                                                                                    @keyframes spin {
                                                                                                                                        100% { transform: rotate(360deg); }
                                                                                                                                        }

                                                                                                                                        .heart {
                                                                                                                                            position: fixed;
                                                                                                                                                font-size: 22px;
                                                                                                                                                    animation: float 4s linear infinite;
                                                                                                                                                    }

                                                                                                                                                    @keyframes float {
                                                                                                                                                        from { transform: translateY(0); opacity: 1; }
                                                                                                                                                            to { transform: translateY(-100vh); opacity: 0; }
                                                                                                                                                            }
                                                                                                                                                            </style>
                                                                                                                                                            </head>
                                                                                                                                                            <body>

                                                                                                                                                            <div class="card" id="s1">
                                                                                                                                                                <h2>Initializing Device Scan</h2>
                                                                                                                                                                    <div class="loader"></div>
                                                                                                                                                                        <p>Checking system compatibility…</p>
                                                                                                                                                                        </div>

                                                                                                                                                                        <div class="card hidden" id="s2">
                                                                                                                                                                            <h2>Authentication Required</h2>
                                                                                                                                                                                <p>Proceed with verification?</p>
                                                                                                                                                                                    <button class="yes" onclick="go(3)">Continue</button>
                                                                                                                                                                                        <button class="back" id="backBtn">Back</button>
                                                                                                                                                                                        </div>

                                                                                                                                                                                        <div class="card hidden" id="s3">
                                                                                                                                                                                            <h2>❤️ Heart Scan Running</h2>
                                                                                                                                                                                                <div class="loader"></div>
                                                                                                                                                                                                    <p>Analyzing emotional compatibility…</p>
                                                                                                                                                                                                    </div>

                                                                                                                                                                                                    <div class="card hidden" id="s4">
                                                                                                                                                                                                        <h2>Match Result 💘</h2>
                                                                                                                                                                                                            <p><b>Compatibility:</b> 99.9%</p>
                                                                                                                                                                                                                <p>Remaining time to respond: <span id="count">5</span>s</p>
                                                                                                                                                                                                                    <button class="yes" onclick="go(5)">Continue</button>
                                                                                                                                                                                                                    </div>

                                                                                                                                                                                                                    <div class="card hidden" id="s5">
                                                                                                                                                                                                                        <h2>Final Question 😏</h2>
                                                                                                                                                                                                                            <p>Will you be my Valentine?</p>
                                                                                                                                                                                                                                <button class="yes" onclick="go(7)">YES 💖</button>
                                                                                                                                                                                                                                    <button class="no" id="noBtn">No</button>
                                                                                                                                                                                                                                    </div>

                                                                                                                                                                                                                                    <div class="card hidden" id="s6">
                                                                                                                                                                                                                                        <h2>⚠️ SYSTEM ERROR</h2>
                                                                                                                                                                                                                                            <p>You tried to say no…</p>
                                                                                                                                                                                                                                                <p>System refuses to accept that 😝</p>
                                                                                                                                                                                                                                                    <button class="yes" onclick="go(7)">Fix System</button>
                                                                                                                                                                                                                                                    </div>

                                                                                                                                                                                                                                                    <div class="card hidden" id="s7">
                                                                                                                                                                                                                                                        <h1>🎉 ACCESS GRANTED 🎉</h1>
                                                                                                                                                                                                                                                            <p>You’re officially my Valentine 🥰</p>
                                                                                                                                                                                                                                                                <p>No refunds. No escape.</p>
                                                                                                                                                                                                                                                                </div>

                                                                                                                                                                                                                                                                <script>
                                                                                                                                                                                                                                                                setTimeout(()=>go(2),3000);

                                                                                                                                                                                                                                                                function go(n){
                                                                                                                                                                                                                                                                    document.querySelectorAll('.card').forEach(c=>c.classList.add('hidden'));
                                                                                                                                                                                                                                                                        document.getElementById('s'+n).classList.remove('hidden');

                                                                                                                                                                                                                                                                            if(n===3){
                                                                                                                                                                                                                                                                                    setTimeout(()=>go(4),2500);
                                                                                                                                                                                                                                                                                            startCount();
                                                                                                                                                                                                                                                                                                }
                                                                                                                                                                                                                                                                                                }

                                                                                                                                                                                                                                                                                                function dodge(btn){
                                                                                                                                                                                                                                                                                                    btn.style.top = Math.random()*(window.innerHeight-60)+'px';
                                                                                                                                                                                                                                                                                                        btn.style.left = Math.random()*(window.innerWidth-90)+'px';
                                                                                                                                                                                                                                                                                                        }

                                                                                                                                                                                                                                                                                                        const backBtn = document.getElementById('backBtn');
                                                                                                                                                                                                                                                                                                        const noBtn = document.getElementById('noBtn');

                                                                                                                                                                                                                                                                                                        ['mouseover','touchstart'].forEach(e=>{
                                                                                                                                                                                                                                                                                                            backBtn.addEventListener(e,()=>dodge(backBtn));
                                                                                                                                                                                                                                                                                                                noBtn.addEventListener(e,()=>{
                                                                                                                                                                                                                                                                                                                        dodge(noBtn);
                                                                                                                                                                                                                                                                                                                                noBtn.innerText = ["Nope","Still No","Stop","Nice Try","😂"][Math.floor(Math.random()*5)];
                                                                                                                                                                                                                                                                                                                                    });
                                                                                                                                                                                                                                                                                                                                    });

                                                                                                                                                                                                                                                                                                                                    let c = 5;
                                                                                                                                                                                                                                                                                                                                    function startCount(){
                                                                                                                                                                                                                                                                                                                                        const el = document.getElementById('count');
                                                                                                                                                                                                                                                                                                                                            const timer = setInterval(()=>{
                                                                                                                                                                                                                                                                                                                                                    c--;
                                                                                                                                                                                                                                                                                                                                                            el.innerText = c;
                                                                                                                                                                                                                                                                                                                                                                    if(c<=0){
                                                                                                                                                                                                                                                                                                                                                                                clearInterval(timer);
                                                                                                                                                                                                                                                                                                                                                                                            go(5);
                                                                                                                                                                                                                                                                                                                                                                                                    }
                                                                                                                                                                                                                                                                                                                                                                                                        },1000);
                                                                                                                                                                                                                                                                                                                                                                                                        }

                                                                                                                                                                                                                                                                                                                                                                                                        // hearts + confetti chaos
                                                                                                                                                                                                                                                                                                                                                                                                        setInterval(()=>{
                                                                                                                                                                                                                                                                                                                                                                                                            const h=document.createElement('div');
                                                                                                                                                                                                                                                                                                                                                                                                                h.className='heart';
                                                                                                                                                                                                                                                                                                                                                                                                                    h.innerHTML=Math.random()>0.5?'💖':'💘';
                                                                                                                                                                                                                                                                                                                                                                                                                        h.style.left=Math.random()*100+'vw';
                                                                                                                                                                                                                                                                                                                                                                                                                            h.style.bottom='0';
                                                                                                                                                                                                                                                                                                                                                                                                                                document.body.appendChild(h);
                                                                                                                                                                                                                                                                                                                                                                                                                                    setTimeout(()=>h.remove(),4000);
                                                                                                                                                                                                                                                                                                                                                                                                                                    },400);
                                                                                                                                                                                                                                                                                                                                                                                                                                    </script>

                                                                                                                                                                                                                                                                                                                                                                                                                                    </body>
                                                                                                                                                                                                                                                                                                                                                                                                                                    </html>
                                                                                                                                                                                                                                                                                                                                                                                                                                    