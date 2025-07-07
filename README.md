# Brain_coin_bot
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Brain Coin - Collect Free Crypto</title>
    <link rel="stylesheet" href="css/style.css">
    <link rel="stylesheet" href="css/animations.css">
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
</head>
<body>
    <div class="container">
        <header>
            <h1>🧠 Brain Coin</h1>
            <div class="wallet">
                <span id="coin-balance">0</span> BRAIN
                <div class="wallet-icon">💰</div>
            </div>
        </header>

        <main>
            <div class="coin-container">
                <div class="coin" id="main-coin">🧠</div>
                <div class="click-text">Tap to collect!</div>
            </div>

            <div class="stats">
                <div class="stat">
                    <span id="coins-per-tap">1</span> per tap
                </div>
                <div class="stat">
                    <span id="coins-per-sec">0</span> per second
                </div>
            </div>
        </main>

        <nav>
            <button onclick="location.href='upgrades.html'">🛠️ Upgrades</button>
            <button onclick="location.href='tasks.html'">✅ Tasks</button>
            <button onclick="showReferral()">👥 Refer Friends</button>
        </nav>
    </div>

    <script src="js/app.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Same head as index.html -->
</head>
<body>
    <div class="container">
        <header>
            <h1>🛠️ Brain Upgrades</h1>
            <div class="wallet">
                <span id="coin-balance">0</span> BRAIN
            </div>
        </header>

        <main>
            <div class="upgrades-grid">
                <!-- Upgrade cards will be generated here -->
            </div>
        </main>

        <nav>
            <button onclick="location.href='index.html'">🏠 Home</button>
            <button onclick="location.href='tasks.html'">✅ Tasks</button>
        </nav>
    </div>

    <script src="js/upgrades.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Same head as index.html -->
</head>
<body>
    <div class="container">
        <header>
            <h1>✅ Brain Tasks</h1>
            <div class="wallet">
                <span id="coin-balance">0</span> BRAIN
            </div>
        </header>

        <main>
            <div class="task-list">
                <div class="task" id="telegram-task">
                    <h3>Join Telegram Channel</h3>
                    <p>+500 BRAIN</p>
                    <button class="task-button" onclick="completeTelegramTask()">Complete</button>
                </div>

                <div class="task" id="youtube-task">
                    <h3>Subscribe & Watch Video</h3>
                    <p>+1000 BRAIN</p>
                    <div class="video-container">
                        <iframe id="youtube-video" src="https://www.youtube.com/embed/YOUR_VIDEO_ID" frameborder="0" allowfullscreen></iframe>
                    </div>
                    <button class="task-button" onclick="completeYoutubeTask()">Complete</button>
                </div>

                <div class="task" id="bot-task">
                    <h3>Start Telegram Bot</h3>
                    <p>+300 BRAIN</p>
                    <button class="task-button" onclick="openTelegramBot()">Complete</button>
                </div>
            </div>
        </main>

        <nav>
            <button onclick="location.href='index.html'">🏠 Home</button>
            <button onclick="location.href='upgrades.html'">🛠️ Upgrades</button>
        </nav>
    </div>

    <script src="js/tasks.js"></script>
</body>
</html> 
/* Base Styles */
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: linear-gradient(135deg, #1a1a2e, #16213e);
    color: white;
    margin: 0;
    padding: 0;
    height: 100vh;
}

.container {
    max-width: 500px;
    margin: 0 auto;
    padding: 20px;
    height: 100%;
    display: flex;
    flex-direction: column;
}

header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}

.wallet {
    background: rgba(255, 255, 255, 0.1);
    padding: 10px 15px;
    border-radius: 20px;
    display: flex;
    align-items: center;
    gap: 8px;
}

/* Coin Styles */
.coin-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    flex-grow: 1;
}

.coin {
    font-size: 80px;
    cursor: pointer;
    transition: transform 0.1s;
    user-select: none;
}

.click-text {
    margin-top: 10px;
    opacity: 0.8;
}

/* Stats */
.stats {
    display: flex;
    justify-content: space-around;
    margin: 30px 0;
}

.stat {
    background: rgba(0, 0, 0, 0.3);
    padding: 15px;
    border-radius: 10px;
    text-align: center;
    min-width: 120px;
}

/* Navigation */
nav {
    display: flex;
    justify-content: space-around;
    padding: 15px 0;
}

nav button {
    background: #4e54c8;
    color: white;
    border: none;
    padding: 12px 20px;
    border-radius: 25px;
    cursor: pointer;
    font-weight: bold;
    transition: background 0.3s;
}

nav button:hover {
    background: #6a6fd8;
}

/* Upgrades Page */
.upgrades-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 15px;
}

.upgrade-card {
    background: rgba(255, 255, 255, 0.1);
    border-radius: 10px;
    padding: 15px;
    text-align: center;
    transition: transform 0.3s;
}

.upgrade-card:hover {
    transform: scale(1.03);
}

.upgrade-card h3 {
    margin-top: 0;
}

.upgrade-card button {
    background: #4CAF50;
    color: white;
    border: none;
    padding: 8px 15px;
    border-radius: 5px;
    cursor: pointer;
    margin-top: 10px;
}

/* Tasks Page */
.task {
    background: rgba(255, 255, 255, 0.1);
    border-radius: 10px;
    padding: 15px;
    margin-bottom: 15px;
}

.task-button {
    background: #FF9800;
    color: white;
    border: none;
    padding: 10px 15px;
    border-radius: 5px;
    cursor: pointer;
    width: 100%;
    font-weight: bold;
}

.video-container {
    position: relative;
    padding-bottom: 56.25%; /* 16:9 */
    height: 0;
    margin: 15px 0;
}

.video-container iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border-radius: 5px;
}
// Initialize Telegram WebApp
const tg = window.Telegram.WebApp;
tg.expand();

// Game State
let state = {
    coins: 0,
    coinsPerTap: 1,
    coinsPerSec: 0,
    upgrades: {},
    completedTasks: []
};

// Load saved game
function loadGame() {
    const saved = localStorage.getItem('brainCoinSave');
    if (saved) {
        state = JSON.parse(saved);
        updateUI();
    }
}

// Save game
function saveGame() {
    localStorage.setItem('brainCoinSave', JSON.stringify(state));
}

// Update all UI elements
function updateUI() {
    document.getElementById('coin-balance').textContent = state.coins.toFixed(2);
    document.getElementById('coins-per-tap').textContent = state.coinsPerTap.toFixed(1);
    document.getElementById('coins-per-sec').textContent = state.coinsPerSec.toFixed(1);
}

// Collect coins
function collectCoins() {
    state.coins += state.coinsPerTap;
    updateUI();
    saveGame();
    
    // Create floating coin animation
    createFloatingCoin();
}

// Create floating coin animation
function createFloatingCoin() {
    const coin = document.createElement('div');
    coin.className = 'floating-coin';
    coin.textContent = '+' + state.coinsPerTap.toFixed(1);
    coin.style.left = Math.random() * 80 + 10 + '%';
    document.querySelector('.coin-container').appendChild(coin);
    
    setTimeout(() => {
        coin.remove();
    }, 1000);
}

// Passive income
setInterval(() => {
    state.coins += state.coinsPerSec / 10;
    updateUI();
    saveGame();
}, 100);

// Initialize
document.getElementById('main-coin').addEventListener('click', collectCoins);
loadGame();

// Show referral
function showReferral() {
    tg.showAlert(`Share your referral link to earn more coins: https://t.me/brain_coin_2025_bot?start=ref_${tg.initDataUnsafe.user.id}`);
}
// Load game state
loadGame();

// Upgrade definitions
const upgrades = [
    {
        id: 'click_power',
        name: 'Click Power',
        description: 'Increase coins per tap',
        basePrice: 10,
        priceGrowth: 1.15,
        effect: () => state.coinsPerTap += 0.5,
        emoji: '🖱️'
    },
    {
        id: 'passive_income',
        name: 'Passive Income',
        description: 'Earn coins automatically',
        basePrice: 25,
        priceGrowth: 1.2,
        effect: () => state.coinsPerSec += 0.1,
        emoji: '⏳'
    },
    {
        id: 'neuron_boost',
        name: 'Neuron Boost',
        description: 'Supercharge your brain power',
        basePrice: 100,
        priceGrowth: 1.25,
        effect: () => {
            state.coinsPerTap += 2;
            state.coinsPerSec += 0.5;
        },
        emoji: '⚡'
    },
    {
        id: 'quantum_brain',
        name: 'Quantum Brain',
        description: 'Think in multiple dimensions',
        basePrice: 500,
        priceGrowth: 1.3,
        effect: () => {
            state.coinsPerSec *= 2;
        },
        emoji: '🌀'
    }
];

// Render upgrades
function renderUpgrades() {
    const grid = document.querySelector('.upgrades-grid');
    grid.innerHTML = '';
    
    upgrades.forEach(upgrade => {
        const owned = state.upgrades[upgrade.id] || 0;
        const price = Math.floor(upgrade.basePrice * Math.pow(upgrade.priceGrowth, owned));
        
        const card = document.createElement('div');
        card.className = 'upgrade-card';
        card.innerHTML = `
            <h3>${upgrade.emoji} ${upgrade.name}</h3>
            <p>${upgrade.description}</p>
            <p>Owned: ${owned}</p>
            <p>Price: ${price} BRAIN</p>
            <button onclick="buyUpgrade('${upgrade.id}')">Buy</button>
        `;
        
        grid.appendChild(card);
    });
}

// Buy upgrade
function buyUpgrade(id) {
    const upgrade = upgrades.find(u => u.id === id);
    const owned = state.upgrades[id] || 0;
    const price = Math.floor(upgrade.basePrice * Math.pow(upgrade.priceGrowth, owned));
    
    if (state.coins >= price) {
        state.coins -= price;
        upgrade.effect();
        state.upgrades[id] = (state.upgrades[id] || 0) + 1;
        updateUI();
        saveGame();
        renderUpgrades();
    } else {
        alert('Not enough BRAIN coins!');
    }
}

// Update UI
function updateUI() {
    document.getElementById('coin-balance').textContent = state.coins.toFixed(2);
}

// Initialize
renderUpgrades();
// Load game state
loadGame();

// Update UI
function updateUI() {
    document.getElementById('coin-balance').textContent = state.coins.toFixed(2);
}

// Complete Telegram task
function completeTelegramTask() {
    if (state.completedTasks.includes('telegram')) {
        alert('You already completed this task!');
        return;
    }
    
    // In a real app, you would verify the user actually joined
    state.coins += 500;
    state.completedTasks.push('telegram');
    document.getElementById('telegram-task').style.opacity = '0.6';
    updateUI();
    saveGame();
    alert('+500 BRAIN for joining our Telegram channel!');
}

// Complete YouTube task
function completeYoutubeTask() {
    if (state.completedTasks.includes('youtube')) {
        alert('You already completed this task!');
        return;
    }
    
    // In a real app, verify with YouTube API
    state.coins += 1000;
    state.completedTasks.push('youtube');
    document.getElementById('youtube-task').style.opacity = '0.6';
    updateUI();
    saveGame();
    alert('+1000 BRAIN for subscribing and watching!');
}

// Open Telegram bot
function openTelegramBot() {
    if (state.completedTasks.includes('bot')) {
        alert('You already completed this task!');
        return;
    }
    
    window.open('https://t.me/Brain_coin_2025_bot', '_blank');
    state.coins += 300;
    state.completedTasks.push('bot');
    document.getElementById('bot-task').style.opacity = '0.6';
    updateUI();
    saveGame();
    alert('+300 BRAIN for starting our bot!');
}

// Initialize
if (state.completedTasks.includes('telegram')) {
    document.getElementById('telegram-task').style.opacity = '0.6';
}
if (state.completedTasks.includes('youtube')) {
    document.getElementById('youtube-task').style.opacity = '0.6';
}
if (state.completedTasks.includes('bot')) {
    document.getElementById('bot-task').style.opacity = '0.6';
}
/* Coin click animation */
.coin:active {
    transform: scale(0.9);
}

/* Floating coin animation */
.floating-coin {
    position: absolute;
    font-size: 20px;
    font-weight: bold;
    color: #FFD700;
    text-shadow: 0 0 5px rgba(0, 0, 0, 0.5);
    animation: float-up 1s ease-out forwards;
    pointer-events: none;
    z-index: 100;
}

@keyframes float-up {
    0% {
        transform: translateY(0);
        opacity: 1;
    }
    100% {
        transform: translateY(-100px);
        opacity: 0;
    }
}

/* Pulse animation for new items */
@keyframes pulse {
    0% { transform: scale(1); }
    50% { transform: scale(1.05); }
    100% { transform: scale(1); }
}

.new-item {
    animation: pulse 2s infinite;
}
