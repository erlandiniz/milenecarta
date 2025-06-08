<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Carta para Minha Querida Filha</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;700&display=swap');
        @import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');
        
        body {
            background-color: #f0e6d2;
            background-image: 
                url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><text x="10" y="20" font-family="Press Start 2P" font-size="10" fill="rgba(0,0,0,0.05)">♥</text></svg>'),
                url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><text x="70" y="80" font-family="Press Start 2P" font-size="12" fill="rgba(0,0,0,0.05)">☆</text></svg>');
            margin: 0;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            font-family: 'Dancing Script', cursive;
            color: #5a3e2a;
        }
        
        .letter-container {
            position: relative;
            max-width: 800px;
            width: 100%;
            background-color: #fff9e6;
            border: 2px solid #d4a76a;
            border-radius: 5px;
            box-shadow: 0 0 20px rgba(0,0,0,0.1);
            padding: 40px;
            margin: 20px;
        }
        
        .letter-container::before, .letter-container::after {
            content: "";
            position: absolute;
            width: 100px;
            height: 100px;
            background-size: contain;
            background-repeat: no-repeat;
            opacity: 0.2;
            z-index: 0;
        }
        
        .letter-container::before {
            top: 10px;
            left: 10px;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><text x="10" y="60" font-family="Press Start 2P" font-size="60" fill="%23d4a76a">☺</text></svg>');
        }
        
        .letter-container::after {
            bottom: 10px;
            right: 10px;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><text x="10" y="80" font-family="Press Start 2P" font-size="80" fill="%23d4a76a">♫</text></svg>');
        }
        
        .letter-content {
            position: relative;
            z-index: 1;
        }
        
        h1 {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 30px;
            color: #8b5a2b;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
        }
        
        p {
            font-size: 1.5rem;
            line-height: 1.6;
            margin-bottom: 20px;
            text-align: justify;
        }
        
        .signature {
            font-size: 2rem;
            text-align: right;
            margin-top: 40px;
            font-weight: bold;
        }
        
        .date {
            font-size: 1.2rem;
            text-align: right;
            margin-top: 10px;
            font-style: italic;
        }
        
        .retro-decoration {
            font-family: 'Press Start 2P', cursive;
            font-size: 0.8rem;
            color: #8b5a2b;
            margin: 20px 0;
            text-align: center;
        }
        
        .music-controls {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 30px;
        }
        
        .retro-button {
            font-family: 'Press Start 2P', cursive;
            font-size: 0.7rem;
            padding: 8px 15px;
            background-color: #d4a76a;
            border: none;
            border-radius: 5px;
            color: white;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .retro-button:hover {
            background-color: #8b5a2b;
            transform: translateY(-2px);
        }
        
        .photo-album {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
            margin: 30px 0;
        }
        
        .photo-placeholder {
            width: 100px;
            height: 100px;
            background-color: #f0e6d2;
            border: 2px dashed #d4a76a;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Press Start 2P', cursive;
            font-size: 0.6rem;
            color: #8b5a2b;
            text-align: center;
            padding: 5px;
        }
        
        .game-container {
            margin: 30px 0;
            text-align: center;
        }
        
        #flappy-bird {
            width: 100%;
            height: 200px;
            background-color: #8fd3f4;
            border: 3px solid #5a3e2a;
            border-radius: 5px;
            position: relative;
            overflow: hidden;
        }
        
        .bird {
            position: absolute;
            width: 30px;
            height: 30px;
            background-color: #ffcc00;
            border-radius: 50%;
            top: 50%;
            left: 50px;
        }
        
        .pipe {
            position: absolute;
            width: 50px;
            background-color: #5cb85c;
            right: -50px;
        }
        
        .score-display {
            font-family: 'Press Start 2P', cursive;
            font-size: 1rem;
            color: #5a3e2a;
            margin-top: 10px;
        }
        
        .hidden-message {
            font-family: 'Press Start 2P', cursive;
            font-size: 0.6rem;
            color: #8b5a2b;
            text-align: center;
            margin-top: 30px;
            cursor: pointer;
        }
        
        .hidden-message:hover {
            text-decoration: underline;
        }
        
        .konami-code {
            display: none;
            font-family: 'Press Start 2P', cursive;
            font-size: 0.8rem;
            color: #d4a76a;
            text-align: center;
            margin-top: 20px;
            animation: blink 1s infinite;
        }
        
        @keyframes blink {
            0% { opacity: 1; }
            50% { opacity: 0.5; }
            100% { opacity: 1; }
        }
    </style>
</head>
<body>
    <div class="letter-container">
        <div class="letter-content">
            <h1>Para Minha Querida Filha</h1>
            
            <div class="retro-decoration">♡ ♡ ♡ ♡ ♡ ♡ ♡ ♡ ♡ ♡ ♡ ♡ ♡ ♡ ♡</div>
            
            <p>Meu amor,</p>
            
            <p>Minha querida Bi, escrevo esta carta de ultima hora pois somos farinha do mesmo saco, e dessa vez não poderia ser diferente, quero apenas diser que te amo incondicionalmente .</p>
            
            <p>Cada dia em sua copahia é um dia especial, você foi pra mim um presente que Deus me prometeu a muito tempo, antes mesmo de eu me entender por gente já tinha o desejo no meu coração de ter uma filha como você.</p>
            
            
            <p>Quero que saiba que, assim como nos melhores jogos, você tem vidas infinitas no meu coração. Pode errar, cair, mas sempre terá a opção de continuar. Eu serei seu botão de "start" sempre que precisar recomeçar.</p>
            
            <div class="retro-decoration">☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆</div>
            
            <p>Nossa relação não tem "game over", apenas pausas para recarregar as energias. E mesmo nos momentos mais difíceis, lembre-se que todo bom jogo tem fases dificeis - são elas que tornam a vitória ainda mais doce.</p>
            
            <div class="game-container">
                <h3>Jogo da Nossa Vida</h3>
                <div id="flappy-bird">
                    <div class="bird"></div>
                </div>
                <div class="score-display">SCORE: ∞</div>
            </div>
            
            <p>Te amo mais do que todos os pontos já conquistados em todos os jogos do mundo juntos. Você é meu high score, meu power-up, meu easter egg mais precioso.</p>
            
            <div class="music-controls">
                <button class="retro-button" onclick="playMusic()">PLAY MUSIC</button>
                <button class="retro-button" onclick="pauseMusic()">PAUSE</button>
                <button class="retro-button" onclick="showMessage()">SECRET</button>
            </div>
            
            <div class="hidden-message" onclick="showKonamiCode()">↑ ↑ ↓ ↓ ← → ← → B A</div>
            <div class="konami-code" id="konami-code">PARABÉNS! VOCÊ DESBLOQUEOU O MODO INFINITO DO MEU AMOR!</div>
            
            <div class="signature">Com todo meu amor,</div>
            <div class="date">Do seu pai, amigo e irmão.</div>
        </div>
    </div>
    
    <audio id="bg-music" loop>
        <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
    </audio>
    
    <script>
        // Controles de música
        const bgMusic = document.getElementById('bg-music');
        
        function playMusic() {
            bgMusic.play();
        }
        
        function pauseMusic() {
            bgMusic.pause();
        }
        
        // Mensagem secreta
        function showMessage() {
            alert("Você encontrou um segredo! Eu te amo mais do que palavras podem expressar!");
        }
        
        // Easter Egg do Código Konami
        const konamiCode = ['ArrowUp', 'ArrowUp', 'ArrowDown', 'ArrowDown', 'ArrowLeft', 'ArrowRight', 'ArrowLeft', 'ArrowRight', 'b', 'a'];
        let konamiIndex = 0;
        
        document.addEventListener('keydown', function(e) {
            if (e.key === konamiCode[konamiIndex]) {
                konamiIndex++;
                if (konamiIndex === konamiCode.length) {
                    showKonamiCode();
                    konamiIndex = 0;
                }
            } else {
                konamiIndex = 0;
            }
        });
        
        function showKonamiCode() {
            const element = document.getElementById('konami-code');
            element.style.display = 'block';
            setTimeout(() => {
                element.style.display = 'none';
            }, 5000);
        }
        
        // Mini-jogo Flappy Bird simplificado
        const bird = document.querySelector('.bird');
        const gameArea = document.getElementById('flappy-bird');
        let birdPosition = 100;
        let gravity = 2;
        let gameRunning = false;
        
        function startGame() {
            if (!gameRunning) {
                gameRunning = true;
                birdPosition = 100;
                bird.style.top = birdPosition + 'px';
                gameLoop();
            }
        }
        
        function gameLoop() {
            if (!gameRunning) return;
            
            birdPosition += gravity;
            bird.style.top = birdPosition + 'px';
            
            if (birdPosition > 170 || birdPosition < 0) {
                gameRunning = false;
                birdPosition = 100;
                bird.style.top = birdPosition + 'px';
            } else {
                requestAnimationFrame(gameLoop);
            }
        }
        
        gameArea.addEventListener('click', function() {
            if (!gameRunning) {
                startGame();
            }
            birdPosition -= 30;
        });
    </script>
</body>
</html>

