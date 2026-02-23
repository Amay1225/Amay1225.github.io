[index.html](https://github.com/user-attachments/files/25492579/index.html)
<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>言霊バトラー：長文の咆哮</title>
    <link rel="stylesheet" href="style.css">
    <link href="https://fonts.googleapis.com/css2?family=M+PLUS+Rounded+1c:wght@700&family=Noto+Sans+JP:wght@400;700;900&display=swap" rel="stylesheet">
</head>
<body>
    <div id="app">
        <header>
            <h1>言霊バトラー <span class="subtitle">長文の咆哮</span></h1>
        </header>
        
        <main>
            <div class="battle-arena">
                <!-- CPU Info -->
                <div class="player-card cpu">
                    <div class="info">
                        <h2>敵 (CPU)</h2>
                        <div class="hp-text"><span id="cpu-hp">50</span> / 50</div>
                    </div>
                    <div class="hp-bar-container">
                        <div id="cpu-hp-bar" class="hp-bar fill"></div>
                    </div>
                    <div id="cpu-status" class="status-effect"></div>
                </div>

                <!-- Battle Animation Area -->
                <div class="center-stage">
                    <div id="animation-area" class="animation-area">
                        <div id="current-word" class="clashing-word"></div>
                        <div id="damage-popup" class="damage-popup"></div>
                    </div>
                </div>

                <!-- Player Info -->
                <div class="player-card you">
                    <div class="info">
                        <h2>あなた</h2>
                        <div class="hp-text"><span id="player-hp">50</span> / 50</div>
                    </div>
                    <div class="hp-bar-container">
                        <div id="player-hp-bar" class="hp-bar fill"></div>
                    </div>
                    <div id="player-status" class="status-effect"></div>
                </div>
            </div>

            <!-- Turn & Next Char -->
            <div class="game-info">
                <div class="next-char-board">
                    次の文字: <span id="next-char" class="highlight">シ</span>
                </div>
                <div id="message-log" class="message-log">バトル開始！あなたが先攻です。（最初は「シ」から）</div>
            </div>

            <!-- History -->
            <div class="history-container">
                <h3>言霊履歴</h3>
                <ul id="history-list">
                    <!-- History injected here -->
                </ul>
            </div>

            <!-- Input Area -->
            <div class="input-area">
                <form id="word-form">
                    <input type="text" id="word-input" autocomplete="off" placeholder="カタカナ・ひらがなで入力（例：シリトリ）" required>
                    <button type="submit" id="submit-btn" class="glow-on-hover">発動</button>
                </form>
            </div>
            
            <!-- Result Screen -->
            <div id="result-screen" class="hidden">
                <h2 id="result-title">Victory!</h2>
                <p id="result-reason"></p>
                <button id="restart-btn">もう一度挑む</button>
            </div>
        </main>
    </div>
    <script src="script.js"></script>
</body>
</html>
