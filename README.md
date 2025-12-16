<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Azmat Hashaan - Profile</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Lato:wght@300;400&display=swap');
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    
    body {
        font-family: 'Lato', sans-serif;
        background: linear-gradient(135deg, #ffeef8 0%, #fff5f0 50%, #ffe8e0 100%);
        color: #5a4a42;
        overflow-x: hidden;
        position: relative;
        min-height: 100vh;
    }
    
    /* Cherry Blossom Tree */
    .tree-container {
        position: fixed;
        right: 0;
        top: 0;
        width: 300px;
        height: 100vh;
        pointer-events: none;
        z-index: 1;
    }
    
    .tree {
        position: absolute;
        right: 0;
        bottom: 0;
        width: 100%;
        height: 100%;
    }
    
    .branch {
        position: absolute;
        background: linear-gradient(180deg, #8B6F47 0%, #654321 100%);
        transform-origin: bottom center;
    }
    
    .trunk {
        width: 40px;
        height: 100%;
        right: 60px;
        bottom: 0;
        border-radius: 20px 20px 0 0;
    }
    
    .branch-1 {
        width: 120px;
        height: 8px;
        right: 80px;
        bottom: 70%;
        transform: rotate(-35deg);
        border-radius: 10px;
    }
    
    .branch-2 {
        width: 140px;
        height: 8px;
        right: 60px;
        bottom: 60%;
        transform: rotate(-45deg);
        border-radius: 10px;
    }
    
    .branch-3 {
        width: 100px;
        height: 8px;
        right: 90px;
        bottom: 50%;
        transform: rotate(-30deg);
        border-radius: 10px;
    }
    
    .branch-4 {
        width: 110px;
        height: 8px;
        right: 70px;
        bottom: 40%;
        transform: rotate(-40deg);
        border-radius: 10px;
    }
    
    .branch-5 {
        width: 90px;
        height: 8px;
        right: 100px;
        bottom: 30%;
        transform: rotate(-25deg);
        border-radius: 10px;
    }
    
    /* Cherry Blossoms on Branches */
    .blossom-cluster {
        position: absolute;
        width: 60px;
        height: 60px;
    }
    
    .cluster-1 { right: 120px; bottom: 72%; }
    .cluster-2 { right: 140px; bottom: 62%; }
    .cluster-3 { right: 110px; bottom: 52%; }
    .cluster-4 { right: 130px; bottom: 42%; }
    .cluster-5 { right: 100px; bottom: 32%; }
    
    .static-blossom {
        position: absolute;
        width: 20px;
        height: 20px;
        background: radial-gradient(circle, #ffb3d9 0%, #ff8fc7 50%, #ff6bb5 100%);
        border-radius: 50% 0 50% 0;
        animation: bloom 3s ease-in-out infinite;
    }
    
    .static-blossom:nth-child(1) { top: 0; left: 0; animation-delay: 0s; }
    .static-blossom:nth-child(2) { top: 10px; left: 20px; animation-delay: 0.5s; transform: rotate(72deg); }
    .static-blossom:nth-child(3) { top: 30px; left: 10px; animation-delay: 1s; transform: rotate(144deg); }
    .static-blossom:nth-child(4) { top: 20px; left: -10px; animation-delay: 1.5s; transform: rotate(216deg); }
    .static-blossom:nth-child(5) { top: 5px; left: 30px; animation-delay: 2s; transform: rotate(288deg); }
    
    @keyframes bloom {
        0%, 100% { transform: scale(1); opacity: 0.9; }
        50% { transform: scale(1.1); opacity: 1; }
    }
    
    /* Falling Petals */
    .petal {
        position: fixed;
        width: 12px;
        height: 12px;
        background: radial-gradient(circle, #ffb3d9 0%, #ff8fc7 100%);
        border-radius: 50% 0 50% 0;
        opacity: 0;
        pointer-events: none;
        z-index: 9999;
        animation: fall linear infinite;
    }
    
    @keyframes fall {
        0% {
            opacity: 0;
            transform: translateY(-20px) translateX(0) rotate(0deg);
        }
        10% {
            opacity: 1;
        }
        90% {
            opacity: 1;
        }
        100% {
            opacity: 0;
            transform: translateY(100vh) translateX(100px) rotate(360deg);
        }
    }
    
    /* Main Container */
    .container {
        max-width: 900px;
        margin: 0 auto;
        padding: 80px 40px;
        position: relative;
        z-index: 2;
    }
    
    /* Header */
    .header {
        text-align: center;
        margin-bottom: 80px;
        animation: fadeInDown 1s ease;
    }
    
    @keyframes fadeInDown {
        from {
            opacity: 0;
            transform: translateY(-30px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }
    
    .name {
        font-family: 'Playfair Display', serif;
        font-size: 4rem;
        font-weight: 700;
        color: #8d5d4f;
        margin-bottom: 20px;
        letter-spacing: 2px;
    }
    
    .tagline {
        font-size: 1.3rem;
        color: #a67c6d;
        font-weight: 300;
        font-style: italic;
        letter-spacing: 1px;
    }
    
    /* Divider */
    .divider {
        width: 150px;
        height: 2px;
        background: linear-gradient(90deg, transparent, #ffb3d9, transparent);
        margin: 60px auto;
    }
    
    /* Content Sections */
    .section {
        margin: 60px 0;
        animation: fadeIn 1.2s ease;
        background: rgba(255, 255, 255, 0.5);
        padding: 40px;
        border-radius: 20px;
        backdrop-filter: blur(10px);
        box-shadow: 0 8px 32px rgba(255, 179, 217, 0.1);
    }
    
    @keyframes fadeIn {
        from {
            opacity: 0;
            transform: translateY(20px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }
    
    .section-title {
        font-family: 'Playfair Display', serif;
        font-size: 2rem;
        color: #8d5d4f;
        margin-bottom: 25px;
        text-align: center;
    }
    
    .section-content {
        font-size: 1.1rem;
        line-height: 2;
        color: #6d5d56;
        text-align: center;
    }
    
    .section-content p {
        margin: 20px 0;
    }
    
    /* Interests Grid */
    .interests-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        gap: 20px;
        margin-top: 30px;
    }
    
    .interest-item {
        background: rgba(255, 255, 255, 0.7);
        padding: 25px;
        border-radius: 15px;
        text-align: center;
        transition: all 0.3s ease;
        border: 2px solid transparent;
    }
    
    .interest-item:hover {
        transform: translateY(-10px);
        border-color: #ffb3d9;
        box-shadow: 0 10px 30px rgba(255, 179, 217, 0.3);
    }
    
    .interest-icon {
        font-size: 2.5rem;
        margin-bottom: 15px;
    }
    
    .interest-text {
        font-size: 1rem;
        color: #8d5d4f;
        font-weight: 400;
    }
    
    /* Quote */
    .quote {
        font-family: 'Playfair Display', serif;
        font-size: 1.5rem;
        font-style: italic;
        color: #a67c6d;
        text-align: center;
        line-height: 2;
        padding: 30px;
        background: rgba(255, 255, 255, 0.3);
        border-radius: 15px;
        margin: 40px 0;
        border-left: 5px solid #ffb3d9;
    }
    
    /* Social Links */
    .social-links {
        display: flex;
        justify-content: center;
        gap: 30px;
        flex-wrap: wrap;
        margin-top: 30px;
    }
    
    .social-btn {
        display: inline-block;
        padding: 15px 35px;
        background: linear-gradient(135deg, #ffb3d9, #ff8fc7);
        color: white;
        text-decoration: none;
        border-radius: 30px;
        font-weight: 400;
        font-size: 1rem;
        transition: all 0.3s ease;
        box-shadow: 0 4px 15px rgba(255, 179, 217, 0.3);
    }
    
    .social-btn:hover {
        transform: translateY(-3px);
        box-shadow: 0 8px 25px rgba(255, 143, 199, 0.5);
        background: linear-gradient(135deg, #ff8fc7, #ff6bb5);
    }
    
    /* Footer */
    .footer {
        text-align: center;
        padding: 40px 20px;
        font-size: 1rem;
        color: #a67c6d;
        font-style: italic;
    }
    
    @media (max-width: 768px) {
        .name {
            font-size: 2.5rem;
        }
        
        .tree-container {
            width: 200px;
        }
        
        .interests-grid {
            grid-template-columns: 1fr;
        }
    }
</style>
</head>
<body>
    <!-- Cherry Blossom Tree -->
    <div class="tree-container">
        <div class="tree">
            <div class="branch trunk"></div>
            <div class="branch branch-1"></div>
            <div class="branch branch-2"></div>
            <div class="branch branch-3"></div>
            <div class="branch branch-4"></div>
            <div class="branch branch-5"></div>
        <!-- Blossom Clusters -->
        <div class="blossom-cluster cluster-1">
            <div class="static-blossom"></div>
            <div class="static-blossom"></div>
            <div class="static-blossom"></div>
            <div class="static-blossom"></div>
            <div class="static-blossom"></div>
        </div>
        <div class="blossom-cluster cluster-2">
            <div class="static-blossom"></div>
            <div class="static-blossom"></div>
            <div class="static-blossom"></div>
            <div class="static-blossom"></div>
            <div class="static-blossom"></div>
        </div>
        <div class="blossom-cluster cluster-3">
            <div class="static-blossom"></div>
            <div class="static-blossom"></div>
            <div class="static-blossom"></div>
            <div class="static-blossom"></div>
            <div class="static-blossom"></div>
        </div>
        <div class="blossom-cluster cluster-4">
            <div class="static-blossom"></div>
            <div class="static-blossom"></div>
            <div class="static-blossom"></div>
            <div class="static-blossom"></div>
            <div class="static-blossom"></div>
        </div>
        <div class="blossom-cluster cluster-5">
            <div class="static-blossom"></div>
            <div class="static-blossom"></div>
            <div class="static-blossom"></div>
            <div class="static-blossom"></div>
            <div class="static-blossom"></div>
        </div>
    </div>
</div>

<!-- Falling Petals Container -->
<div id="petals-container"></div>

<!-- Main Content -->
<div class="container">
    <div class="header">
        <h1 class="name">Azmat Hashaan</h1>
        <p class="tagline">Living in harmony with the seasons</p>
    </div>
    
    <div class="divider"></div>
    
    <div class="section">
        <h2 class="section-title">About Me</h2>
        <div class="section-content">
            <p>I find beauty in the gentle transitions of life, much like the changing seasons.</p>
            <p>Like cherry blossoms that bloom and fall, I embrace each moment with grace and gratitude.</p>
            <p>My journey is about discovering peace in simplicity and wonder in the everyday.</p>
        </div>
    </div>
    
    <div class="divider"></div>
    
    <div class="section">
        <h2 class="section-title">What Brings Me Joy</h2>
        <div class="interests-grid">
            <div class="interest-item">
                <div class="interest-icon">🌸</div>
                <div class="interest-text">Nature & Tranquility</div>
            </div>
            <div class="interest-item">
                <div class="interest-icon">🍵</div>
                <div class="interest-text">Quiet Moments</div>
            </div>
            <div class="interest-item">
                <div class="interest-icon">📖</div>
                <div class="interest-text">Stories & Wisdom</div>
            </div>
            <div class="interest-item">
                <div class="interest-icon">🎨</div>
                <div class="interest-text">Art & Expression</div>
            </div>
            <div class="interest-item">
                <div class="interest-icon">🌅</div>
                <div class="interest-text">Golden Hours</div>
            </div>
            <div class="interest-item">
                <div class="interest-icon">🍂</div>
                <div class="interest-text">Seasonal Changes</div>
            </div>
        </div>
    </div>
    
    <div class="divider"></div>
    
    <div class="quote">
        "Just as cherry blossoms bloom beautifully and fall gracefully, we too must learn to embrace both beginnings and endings with equal serenity."
    </div>
    
    <div class="divider"></div>
    
    <div class="section">
        <h2 class="section-title">Let's Connect</h2>
        <div class="social-links">
            <a href="https://twitter.com/azmathashaan" class="social-btn">Twitter</a>
            <a href="https://instagram.com/azmathashaan" class="social-btn">Instagram</a>
            <a href="https://www.buymeacoffee.com/azmathashaan" class="social-btn">Buy Me A Coffee</a>
        </div>
    </div>
    
    <div class="footer">
        <p>Thank you for visiting my space 🌸</p>
        <p>May your path be filled with beauty and peace</p>
    </div>
</div>

<script>
    // Create falling petals
    function createPetal() {
        const petal = document.createElement('div');
        petal.className = 'petal';
        
        // Random starting position near the tree
        const startX = window.innerWidth - Math.random() * 400;
        const duration = 8 + Math.random() * 7; // 8-15 seconds
        const delay = Math.random() * 5;
        
        petal.style.left = startX + 'px';
        petal.style.animationDuration = duration + 's';
        petal.style.animationDelay = delay + 's';
        
        // Random rotation
        petal.style.transform = `rotate(${Math.random() * 360}deg)`;
        
        document.getElementById('petals-container').appendChild(petal);
        
        // Remove petal after animation
        setTimeout(() => {
            petal.remove();
        }, (duration + delay) * 1000);
    }
    
    // Create petals continuously
    setInterval(createPetal, 400);
    
    // Initial burst of petals
    for (let i = 0; i < 20; i++) {
        setTimeout(createPetal, i * 200);
    }
</script>
</body>
</html>
