<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Azmat Hashaan - Gaming Profile</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&family=Orbitron:wght@400;700;900&display=swap');
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    
    body {
        background: #000;
        color: #fff;
        font-family: 'Orbitron', sans-serif;
        overflow-x: hidden;
        position: relative;
    }
    
    /* Animated Background Particles */
    .particles {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        z-index: 0;
        pointer-events: none;
        opacity: 0.15;
    }
    
    .particle {
        position: absolute;
        width: 4px;
        height: 4px;
        background: linear-gradient(45deg, #ff0000, #ff6b00, #ffd500);
        border-radius: 50%;
        animation: float 15s infinite;
    }
    
    @keyframes float {
        0%, 100% { transform: translateY(0) translateX(0) rotate(0deg); opacity: 0; }
        10% { opacity: 1; }
        90% { opacity: 1; }
        100% { transform: translateY(-1000px) translateX(500px) rotate(360deg); opacity: 0; }
    }
    
    /* Animated Border Frame */
    .border-frame {
        position: fixed;
        pointer-events: none;
        z-index: 9999;
    }
    
    .border-top, .border-bottom {
        width: 100%;
        height: 8px;
        background: linear-gradient(90deg, #ff0000, #ff6b00, #ffd500, #ff6b00, #ff0000);
        background-size: 200% 100%;
        animation: borderGlow 3s linear infinite;
        box-shadow: 0 0 20px #ff0000;
    }
    
    .border-top { top: 0; left: 0; }
    .border-bottom { bottom: 0; left: 0; }
    
    .border-left, .border-right {
        width: 8px;
        height: 100%;
        background: linear-gradient(180deg, #ff0000, #ff6b00, #ffd500, #ff6b00, #ff0000);
        background-size: 100% 200%;
        animation: borderGlow 3s linear infinite;
        box-shadow: 0 0 20px #ff0000;
    }
    
    .border-left { top: 0; left: 0; }
    .border-right { top: 0; right: 0; }
    
    @keyframes borderGlow {
        0% { background-position: 0% 0%; }
        100% { background-position: 200% 200%; }
    }
    
    /* Corner Decorations */
    .corner {
        position: fixed;
        width: 60px;
        height: 60px;
        border: 4px solid #ff0000;
        z-index: 9998;
        pointer-events: none;
        animation: cornerPulse 2s ease-in-out infinite;
    }
    
    .corner-tl { top: 20px; left: 20px; border-right: none; border-bottom: none; }
    .corner-tr { top: 20px; right: 20px; border-left: none; border-bottom: none; }
    .corner-bl { bottom: 20px; left: 20px; border-right: none; border-top: none; }
    .corner-br { bottom: 20px; right: 20px; border-left: none; border-top: none; }
    
    @keyframes cornerPulse {
        0%, 100% { box-shadow: 0 0 10px #ff0000; }
        50% { box-shadow: 0 0 30px #ff0000, 0 0 50px #ff6b00; }
    }
    
    /* Main Container */
    .container {
        position: relative;
        z-index: 1;
        max-width: 1400px;
        margin: 0 auto;
        padding: 60px 40px;
    }
    
    /* Header Section */
    .header {
        text-align: center;
        margin-bottom: 80px;
        position: relative;
    }
    
    .glitch-wrapper {
        position: relative;
        display: inline-block;
    }
    
    .glitch {
        font-family: 'Press Start 2P', cursive;
        font-size: 4rem;
        font-weight: 900;
        color: #fff;
        text-shadow: 0 0 10px #ff0000, 0 0 20px #ff6b00, 0 0 30px #ffd500;
        animation: glitch 1s infinite;
        letter-spacing: 8px;
        margin-bottom: 20px;
    }
    
    @keyframes glitch {
        0% { text-shadow: 0 0 10px #ff0000, 0 0 20px #ff6b00; }
        25% { text-shadow: -2px 0 10px #ff0000, 2px 2px 20px #ff6b00; }
        50% { text-shadow: 2px 0 10px #ff0000, -2px -2px 20px #ffd500; }
        75% { text-shadow: -2px 0 10px #ffd500, 2px 2px 20px #ff0000; }
        100% { text-shadow: 0 0 10px #ff0000, 0 0 20px #ff6b00; }
    }
    
    .subtitle {
        font-size: 1.5rem;
        color: #ffd500;
        text-transform: uppercase;
        letter-spacing: 4px;
        margin-top: 20px;
        animation: fadeInOut 3s ease-in-out infinite;
    }
    
    @keyframes fadeInOut {
        0%, 100% { opacity: 0.6; }
        50% { opacity: 1; }
    }
    
    .fitgirl-badge {
        display: inline-block;
        background: linear-gradient(135deg, #ff0066, #cc0052);
        color: #fff;
        padding: 15px 40px;
        border-radius: 50px;
        font-size: 1.2rem;
        font-weight: 900;
        margin-top: 30px;
        text-transform: uppercase;
        letter-spacing: 3px;
        box-shadow: 0 0 30px rgba(255, 0, 102, 0.8), inset 0 0 20px rgba(255, 255, 255, 0.2);
        animation: pulse 2s ease-in-out infinite;
        border: 3px solid #fff;
    }
    
    @keyframes pulse {
        0%, 100% { transform: scale(1); }
        50% { transform: scale(1.05); box-shadow: 0 0 50px rgba(255, 0, 102, 1); }
    }
    
    .stats-bar {
        display: flex;
        justify-content: center;
        gap: 30px;
        margin-top: 40px;
        flex-wrap: wrap;
    }
    
    .stat-item {
        background: rgba(255, 0, 0, 0.1);
        border: 2px solid #ff0000;
        padding: 15px 30px;
        border-radius: 10px;
        font-weight: 700;
        text-transform: uppercase;
        font-size: 0.9rem;
        letter-spacing: 2px;
        transition: all 0.3s ease;
        box-shadow: 0 0 20px rgba(255, 0, 0, 0.3);
    }
    
    .stat-item:hover {
        background: rgba(255, 0, 0, 0.3);
        transform: translateY(-5px);
        box-shadow: 0 5px 30px rgba(255, 0, 0, 0.6);
    }
    
    /* About Section */
    .about {
        text-align: center;
        margin: 80px 0;
        padding: 40px;
        background: rgba(255, 255, 255, 0.03);
        border-radius: 20px;
        border: 2px solid rgba(255, 107, 0, 0.3);
        position: relative;
        overflow: hidden;
    }
    
    .about::before {
        content: '';
        position: absolute;
        top: -50%;
        left: -50%;
        width: 200%;
        height: 200%;
        background: linear-gradient(45deg, transparent, rgba(255, 0, 0, 0.1), transparent);
        animation: shine 3s linear infinite;
    }
    
    @keyframes shine {
        0% { transform: rotate(0deg); }
        100% { transform: rotate(360deg); }
    }
    
    .about h2 {
        font-size: 2.5rem;
        margin-bottom: 30px;
        position: relative;
        z-index: 1;
        color: #ffd500;
        text-transform: uppercase;
    }
    
    .about-text {
        font-size: 1.2rem;
        line-height: 2;
        max-width: 900px;
        margin: 0 auto;
        position: relative;
        z-index: 1;
        text-align: left;
    }
    
    .about-text p {
        margin: 15px 0;
        color: #ccc;
    }
    
    .highlight {
        color: #ff6b00;
        font-weight: 700;
    }
    
    /* Game Library */
    .library {
        margin: 100px 0;
    }
    
    .library h2 {
        text-align: center;
        font-size: 3rem;
        margin-bottom: 60px;
        color: #ffd500;
        text-transform: uppercase;
        text-shadow: 0 0 20px #ffd500;
    }
    
    .games-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 40px;
        padding: 20px;
    }
    
    .game-card {
        background: rgba(255, 255, 255, 0.05);
        border-radius: 20px;
        overflow: hidden;
        transition: all 0.4s ease;
        border: 3px solid transparent;
        position: relative;
        cursor: pointer;
    }
    
    .game-card::before {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        border-radius: 20px;
        padding: 3px;
        background: linear-gradient(45deg, #ff0000, #ff6b00, #ffd500);
        -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
        -webkit-mask-composite: xor;
        mask-composite: exclude;
        opacity: 0;
        transition: opacity 0.4s ease;
    }
    
    .game-card:hover::before {
        opacity: 1;
    }
    
    .game-card:hover {
        transform: translateY(-15px) scale(1.05);
        box-shadow: 0 20px 60px rgba(255, 107, 0, 0.6);
    }
    
    .game-poster {
        width: 100%;
        height: 350px;
        object-fit: cover;
        display: block;
    }
    
    .game-info {
        padding: 20px;
        text-align: center;
    }
    
    .game-title {
        font-size: 1.3rem;
        font-weight: 900;
        margin-bottom: 15px;
        color: #fff;
        text-transform: uppercase;
    }
    
    .progress-bar {
        width: 100%;
        height: 8px;
        background: rgba(255, 255, 255, 0.2);
        border-radius: 10px;
        overflow: hidden;
        margin: 15px 0;
    }
    
    .progress-fill {
        height: 100%;
        background: linear-gradient(90deg, #ff0000, #ff6b00, #ffd500);
        border-radius: 10px;
        transition: width 1s ease;
        box-shadow: 0 0 10px #ffd500;
    }
    
    .game-stats {
        display: flex;
        justify-content: space-between;
        margin-top: 15px;
        font-size: 0.9rem;
    }
    
    .hours {
        color: #ff6b00;
        font-weight: 700;
    }
    
    .rating {
        color: #ffd500;
    }
    
    /* Social Links */
    .social-section {
        text-align: center;
        margin: 100px 0;
        padding: 60px 20px;
        background: rgba(255, 0, 0, 0.05);
        border-radius: 30px;
    }
    
    .social-section h2 {
        font-size: 2.5rem;
        margin-bottom: 40px;
        color: #ffd500;
    }
    
    .social-links {
        display: flex;
        justify-content: center;
        gap: 30px;
        flex-wrap: wrap;
    }
    
    .social-btn {
        display: inline-block;
        padding: 18px 40px;
        background: linear-gradient(135deg, #ff0000, #ff6b00);
        color: #fff;
        text-decoration: none;
        border-radius: 50px;
        font-weight: 900;
        font-size: 1.1rem;
        text-transform: uppercase;
        letter-spacing: 2px;
        transition: all 0.3s ease;
        border: 3px solid #fff;
        box-shadow: 0 5px 20px rgba(255, 0, 0, 0.4);
    }
    
    .social-btn:hover {
        transform: translateY(-5px) scale(1.1);
        box-shadow: 0 10px 40px rgba(255, 107, 0, 0.8);
        background: linear-gradient(135deg, #ff6b00, #ffd500);
    }
    
    /* Footer */
    .footer {
        text-align: center;
        padding: 60px 20px;
        font-size: 1.5rem;
        color: #ffd500;
        text-transform: uppercase;
        letter-spacing: 3px;
        font-weight: 700;
        text-shadow: 0 0 20px #ffd500;
    }
    
    /* Floating Icons */
    .floating-icon {
        position: fixed;
        font-size: 3rem;
        opacity: 0.1;
        pointer-events: none;
        z-index: 0;
        animation: floatIcon 20s infinite;
    }
    
    @keyframes floatIcon {
        0%, 100% { transform: translateY(0) rotate(0deg); }
        50% { transform: translateY(-50px) rotate(180deg); }
    }
    
    .icon-1 { top: 10%; left: 5%; animation-delay: 0s; }
    .icon-2 { top: 30%; right: 8%; animation-delay: 2s; }
    .icon-3 { bottom: 20%; left: 10%; animation-delay: 4s; }
    .icon-4 { bottom: 40%; right: 5%; animation-delay: 6s; }
    .icon-5 { top: 60%; left: 15%; animation-delay: 8s; }
    .icon-6 { top: 80%; right: 12%; animation-delay: 10s; }
    
    @media (max-width: 768px) {
        .glitch { font-size: 2rem; }
        .subtitle { font-size: 1rem; }
        .games-grid { grid-template-columns: 1fr; }
    }
</style>
</head>
<body>
    <!-- Animated Border Frame -->
    <div class="border-frame border-top"></div>
    <div class="border-frame border-bottom"></div>
    <div class="border-frame border-left"></div>
    <div class="border-frame border-right"></div>
<!-- Corner Decorations -->
<div class="corner corner-tl"></div>
<div class="corner corner-tr"></div>
<div class="corner corner-bl"></div>
<div class="corner corner-br"></div>

<!-- Background Particles -->
<div class="particles" id="particles"></div>

<!-- Floating Gaming Icons -->
<div class="floating-icon icon-1">🎮</div>
<div class="floating-icon icon-2">🎯</div>
<div class="floating-icon icon-3">🏆</div>
<div class="floating-icon icon-4">⚡</div>
<div class="floating-icon icon-5">🔥</div>
<div class="floating-icon icon-6">💀</div>

<div class="container">
    <!-- Header -->
    <div class="header">
        <div class="glitch-wrapper">
            <h1 class="glitch">AZMAT HASHAAN</h1>
        </div>
        <p class="subtitle">Pro Gamer | Content Creator | Streamer</p>
        <div class="fitgirl-badge">🎮 FitGirl Repack Enthusiast 🎮</div>
        <div class="stats-bar">
            <div class="stat-item">🖥️ PC Master Race</div>
            <div class="stat-item">🟢 Online Now</div>
            <div class="stat-item">👑 Legendary Rank</div>
            <div class="stat-item">⏱️ 10,000+ Hours</div>
        </div>
    </div>
    
    <!-- About Section -->
    <div class="about">
        <h2>💀 Who Am I? 💀</h2>
        <div class="about-text">
            <p><span class="highlight">🎯 Professional Gamer</span> conquering every open world, racing through every track, and dominating every multiplayer lobby.</p>
            <p><span class="highlight">🎮 FitGirl Repack Pro</span> - I know the art of maximizing storage and minimizing download times while keeping the gaming experience pristine.</p>
            <p><span class="highlight">🏎️ Racing Enthusiast | Strategy Master | FPS Legend</span> - Whether it's drifting through Liberty City or surviving in the Wild West, I've mastered them all.</p>
            <p><span class="highlight">🌍 Building My Gaming Empire</span> - One victory at a time, one achievement at a time, one perfectly installed FitGirl repack at a time.</p>
            <p><span class="highlight">💀 Your Worst Nightmare</span> in multiplayer lobbies. GG EZ.</p>
        </div>
    </div>
    
    <!-- Game Library -->
    <div class="library">
        <h2>🎮 STEAM LIBRARY 🎮</h2>
        <div class="games-grid">
            <div class="game-card">
                <img src="https://image.api.playstation.com/vulcan/ap/rnd/202202/2816/6s08SwXVoprpGZdEGKiDbzwn.png" alt="GTA V" class="game-poster">
                <div class="game-info">
                    <div class="game-title">GTA V</div>
                    <div class="progress-bar"><div class="progress-fill" style="width: 100%"></div></div>
                    <div class="game-stats">
                        <span class="hours">⏱️ 1000+ Hours</span>
                        <span class="rating">⭐⭐⭐⭐⭐</span>
                    </div>
                </div>
            </div>
            
            <div class="game-card">
                <img src="https://upload.wikimedia.org/wikipedia/en/b/b7/Grand_Theft_Auto_IV_cover.jpg" alt="GTA IV" class="game-poster">
                <div class="game-info">
                    <div class="game-title">GTA IV</div>
                    <div class="progress-bar"><div class="progress-fill" style="width: 100%"></div></div>
                    <div class="game-stats">
                        <span class="hours">⏱️ 500+ Hours</span>
                        <span class="rating">⭐⭐⭐⭐⭐</span>
                    </div>
                </div>
            </div>
            
            <div class="game-card">
                <img src="https://image.api.playstation.com/vulcan/ap/rnd/202207/1210/4xJ8XB3bi888QTLZYdl7Oi0s.png" alt="Red Dead Redemption 2" class="game-poster">
                <div class="game-info">
                    <div class="game-title">Red Dead Redemption 2</div>
                    <div class="progress-bar"><div class="progress-fill" style="width: 100%"></div></div>
                    <div class="game-stats">
                        <span class="hours">⏱️ 800+ Hours</span>
                        <span class="rating">⭐⭐⭐⭐⭐</span>
                    </div>
                </div>
            </div>
            
            <div class="game-card">
                <img src="https://image.api.playstation.com/cdn/UP0001/CUSA02369_00/GuEKbG0fhE6TKqvJ40vdvelQu5NgGLbW.png" alt="Watch Dogs" class="game-poster">
                <div class="game-info">
                    <div class="game-title">Watch Dogs</div>
                    <div class="progress-bar"><div class="progress-fill" style="width: 100%"></div></div>
                    <div class="game-stats">
                        <span class="hours">⏱️ 300+ Hours</span>
                        <span class="rating">⭐⭐⭐⭐⭐</span>
                    </div>
                </div>
            </div>
            
            <div class="game-card">
                <img src="https://cdn1.epicgames.com/offer/4fe75c537c5b46349ac1eb175b2919c3/EGS_ForzaHorizon5PremiumEdition_PlaygroundGames_Editions_S2_1200x1600-7ab62e90f495b87ce8e0c18c0bd7fc5e" alt="Forza Horizon 5" class="game-poster">
                <div class="game-info">
                    <div class="game-title">Forza Horizon 5</div>
                    <div class="progress-bar"><div class="progress-fill" style="width: 95%"></div></div>
                    <div class="game-stats">
                        <span class="hours">⏱️ 600+ Hours</span>
                        <span class="rating">⭐⭐⭐⭐⭐</span>
                    </div>
                </div>
            </div>
            
            <div class="game-card">
                <img src="https://gaming-cdn.com/images/products/182/616x353/far-cry-3-pc-game-uplay-cover.jpg" alt="Far Cry 3" class="game-poster">
                <div class="game-info">
                    <div class="game-title">Far Cry 3</div>
                    <div class="progress-bar"><div class="progress-fill" style="width: 100%"></div></div>
                    <div class="game-stats">
                        <span class="hours">⏱️ 400+ Hours</span>
                        <span class="rating">⭐⭐⭐⭐⭐</span>
                    </div>
                </div>
            </div>
            
            <div class="game-card">
                <img src="https://image.api.playstation.com/cdn/UP0082/CUSA02740_00/2FEGqKjQ0pXaq89ttes5YzT6y85poGoq.png" alt="Just Cause 3" class="game-poster">
                <div class="game-info">
                    <div class="game-title">Just Cause 3</div>
                    <div class="progress-bar"><div class="progress-fill" style="width: 100%"></div></div>
                    <div class="game-stats">
                        <span class="hours">⏱️ 350+ Hours</span>
                        <span class="rating">⭐⭐⭐⭐⭐</span>
                    </div>
                </div>
            </div>
            
            <div class="game-card">
                <img src="https://gaming-cdn.com/images/products/2865/616x353/need-for-speed-most-wanted-pc-game-origin-cover.jpg" alt="NFS Most Wanted" class="game-poster">
                <div class="game-info">
                    <div class="game-title">NFS Most Wanted</div>
                    <div class="progress-bar"><div class="progress-fill" style="width: 100%"></div></div>
                    <div class="game-stats">
                        <span class="hours">⏱️ 450+ Hours</span>
                        <span class="rating">⭐⭐⭐⭐⭐</span>
                    </div>
                </div>
            </div>
            
            <div class="game-card">
                <img src="https://cdn.cloudflare.steamstatic.com/steam/apps/945360/library_600x900.jpg" alt="Among Us" class="game-poster">
                <div class="game-info">
                    <div class="game-title">Among Us</div>
                    <div class="progress-bar"><div class="progress-fill" style="width: 90%"></div></div>
                    <div class="game-stats">
                        <span class="hours">⏱️ 200+ Hours</span>
                        <span class="rating">⭐⭐⭐⭐</span>
                    </div>
                </div>
            </div>
            
            <div class="game-card">
                <img src="https://image.api.playstation.com/vulcan/ap/rnd/202208/0921/dR9KJAKDW2izPuWoKNqj8FE2.png" alt="Hogwarts Legacy" class="game-poster">
                <div class="game-info">
                    <div class="game-title">Hogwarts Legacy</div>
                    <div class="progress-bar"><div class="progress-fill" style="width: 88%"></div></div>
                    <div class="game-stats">
                        <span class="hours">⏱️ 250+ Hours</span>
                        <span class="rating">⭐⭐⭐⭐⭐</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <!-- Social Section -->
    <div class="social-section">
        <h2>🌐 CONNECT WITH ME 🌐</h2>
        <div class="social-links">
            <a href="https://twitter.com/azmathashaan" class="social-btn">Twitter</a>
            <a href="https://instagram.com/azmathashaan" class="social-btn">Instagram</a>
            <a href="https://twitch.tv/azmathashaan" class="social-btn">Twitch</a>
            <a href="https://youtube.com/@azmathashaan" class="social-btn">YouTube</a>
            <a href="https://discord.gg/azmathashaan" class="social-btn">Discord</a>
            <a href="https://steamcommunity.com/id/azmathashaan" class="social-btn">Steam</a>
        </div>
        <div class="social-links" style="margin-top: 30px;">
            <a href="https://www.buymeacoffee.com/azmathashaan" class="social-btn" style="background: linear-gradient(135deg, #FFDD00, #FFA500);">☕ Buy Me Coffee</a>
            <a href="https://ko-fi.com/azmathashaan" class="social-btn" style="background: linear-gradient(135deg, #FF5E5B, #D9534F);">💖 Ko-fi</a>
            <a href="https://paypal.me/azmathashaan" class="social-btn" style="background: linear-gradient(135deg, #00457C, #0070BA);">💳 PayPal</a>
        </div>
    </div>
    
    <!-- Footer -->
    <div class="footer">
        💀 "GAME OVER? NEVER. RESPAWN AND DOMINATE!" 💀
    </div>
</div>

<script>
    // Generate particles
    const particlesContainer = document.getElementById('particles');
    for (let i = 0; i < 50; i++) {
        const particle = document.createElement('div');
        particle.className = 'particle';
        particle.style.left = Math.random() * 100 + '%';
        particle.style.animationDelay = Math.random() * 15 + 's';
        particle.style.animationDuration = (Math.random() * 10 + 10) + 's';
        particlesContainer.appendChild(particle);
    }
    
    // Animate progress bars on scroll
    const observerOptions = {
        threshold: 0.5
    };
    
    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.style.width = entry.target.getAttribute('data-width') || '100%';
            }
        });
    }, observerOptions);
    
    document.querySelectorAll('.progress-fill').forEach(fill => {
        fill.setAttribute('data-width', fill.style.width);
        fill.style.width = '0%';
        observer.observe(fill);
    });
</script>
</body>
</html>
