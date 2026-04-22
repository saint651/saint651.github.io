<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>THE RULE | Truth & Authority</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700;900&family=Playfair+Display:wght@700;900&family=Lora:ital,wght@0,400;0,700;1,400&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --color-bg: #ffffff;
            --color-text: #1a1a1a;
            --color-accent: #e31e24;
            --color-border: #eeeeee;
            --font-main: 'Montserrat', sans-serif;
            --font-heading: 'Playfair Display', serif;
            --font-body: 'Lora', serif;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { 
            background-color: var(--color-bg); 
            color: var(--color-text); 
            font-family: var(--font-main); 
            line-height: 1.6;
            overflow-x: hidden; /* Prevent horizontal scroll */
        }

        header { border-bottom: 4px solid var(--color-accent); padding: 30px 0; text-align: center; }
        .logo-container { max-width: 1200px; margin: 0 auto; display: flex; flex-direction: column; align-items: center; }
        .logo-img { height: 180px; margin-bottom: 10px; }
        .tagline { font-size: 0.9rem; text-transform: uppercase; letter-spacing: 5px; font-weight: 700; color: #333; margin-top: -20px; }

        nav { border-bottom: 1px solid var(--color-border); background: #fff; position: sticky; top: 0; z-index: 1000; }
        .nav-inner { max-width: 1200px; margin: 0 auto; display: flex; justify-content: center; gap: 30px; padding: 15px 0; flex-wrap: wrap; }
        .nav-inner a { text-decoration: none; color: var(--color-text); font-weight: 700; font-size: 0.85rem; text-transform: uppercase; transition: color 0.3s; }
        .nav-inner a:hover { color: var(--color-accent); }

        .container { max-width: 1200px; margin: 40px auto; display: grid; grid-template-columns: 1fr 350px; gap: 40px; padding: 0 20px; }

        .featured-story { grid-column: 1 / -1; margin-bottom: 40px; border-bottom: 2px solid #000; padding-bottom: 40px; }
        .featured-grid { display: grid; grid-template-columns: 1.5fr 1fr; gap: 40px; }
        
        /* FIXED: Ensure images are fully viewed */
        .featured-img { 
            width: 100%; 
            height: auto; /* Allow full height visibility */
            display: block;
            border-radius: 0; 
            box-shadow: 10px 10px 0px var(--color-accent); 
        }
        
        .featured-content h2 { font-family: var(--font-heading); font-size: 3rem; margin-bottom: 20px; line-height: 1.1; font-weight: 900; }
        .featured-content p { font-family: var(--font-body); font-size: 1.1rem; color: #333; margin-bottom: 15px; }
        .category-tag { background: var(--color-accent); color: #fff; padding: 4px 12px; font-size: 0.75rem; font-weight: 900; text-transform: uppercase; display: inline-block; margin-bottom: 15px; }

        .story-list { display: flex; flex-direction: column; gap: 50px; }
        .story-card { display: grid; grid-template-columns: 350px 1fr; gap: 30px; align-items: start; border-bottom: 1px solid var(--color-border); padding-bottom: 30px; }
        
        /* FIXED: Ensure story images are fully viewed */
        .story-card img { 
            width: 100%; 
            height: auto; /* Allow full height visibility */
            max-height: 400px; /* Optional: prevent extreme verticality */
            object-fit: contain; /* Ensure full image is seen */
            background: #f0f0f0;
        }
        
        .story-card h3 { font-family: var(--font-heading); font-size: 1.8rem; margin-bottom: 15px; line-height: 1.2; }
        .story-card p { font-family: var(--font-body); color: #444; font-size: 1rem; }

        .sidebar-widget { margin-bottom: 50px; background: #f9f9f9; padding: 20px; border-top: 3px solid #000; }
        .widget-title { font-weight: 900; text-transform: uppercase; margin-bottom: 25px; font-size: 1.2rem; letter-spacing: 1px; text-align: center; border-bottom: 1px solid #ddd; padding-bottom: 10px; }
        .trending-item { display: flex; gap: 15px; margin-bottom: 20px; padding-bottom: 15px; border-bottom: 1px solid #eee; }
        .trending-item:last-child { border-bottom: none; }
        .trending-item img { width: 90px; height: 90px; object-fit: cover; }
        .trending-item h4 { font-size: 0.95rem; line-height: 1.3; font-family: var(--font-heading); }

        /* FIXED: Full-width black footer without white box */
        footer { 
            background: #000; 
            color: #fff; 
            padding: 80px 0 40px 0; 
            margin-top: 80px; 
            width: 100vw; /* Force full viewport width */
            position: relative;
            left: 50%;
            right: 50%;
            margin-left: -50vw;
            margin-right: -50vw;
            text-align: center;
        }
        .footer-inner {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        .footer-logo { 
            height: 120px; 
            filter: brightness(0) invert(1); 
            margin-bottom: 30px; 
            display: block;
            margin-left: auto;
            margin-right: auto;
        }
        .footer-links {
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid #333;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 20px;
        }
        .footer-text { 
            font-size: 0.8rem; 
            opacity: 0.8; 
            letter-spacing: 2px; 
            text-transform: uppercase;
            font-weight: 700;
        }
        .footer-tos {
            font-size: 0.8rem;
            opacity: 0.8;
            letter-spacing: 2px;
            text-transform: uppercase;
            font-weight: 700;
            text-decoration: none;
            color: #fff;
        }
        .footer-tos:hover {
            color: var(--color-accent);
        }
        .footer-social {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-bottom: 30px;
            font-size: 1.5rem;
        }
        .footer-social i {
            color: #fff;
            cursor: pointer;
            transition: color 0.3s;
        }
        .footer-social i:hover {
            color: var(--color-accent);
        }

        @media (max-width: 900px) {
            .container { grid-template-columns: 1fr; }
            .featured-grid { grid-template-columns: 1fr; }
            .story-card { grid-template-columns: 1fr; }
            .footer-links { justify-content: center; text-align: center; }
        }
    </style>
</head>
<body>

<header>
    <div class="logo-container">
        <img src="https://files.manuscdn.com/user_upload_by_module/session_file/310519663587410563/YTcqjfynEoJTHdXH.png" alt="The Rule Logo" class="logo-img">
        <div class="tagline">Truth & Authority</div>
    </div>
</header>

<nav>
    <div class="nav-inner">
        <a href="#">Home</a>
        <a href="#">Global News</a>
        <a href="#">African Voices</a>
        <a href="#">Tech & Future</a>
        <a href="#">Culture</a>
        <a href="#">Business</a>
    </div>
</nav>

<div class="container">
    <main class="main-content">
        <!-- Featured Story: Edi Gathegi -->
        <section class="featured-story">
            <div class="featured-grid">
                <img src="https://files.manuscdn.com/user_upload_by_module/session_file/310519663587410563/AElRgHvPgPhhIfFC.png" alt="Edi Gathegi" class="featured-img">
                <div class="featured-content">
                    <span class="category-tag">Cover Story</span>
                    <h2>From Mathare to Netflix – The Journey of Edi Gathegi</h2>
                    <p>Before he appeared on global screens, Edi Gathegi had a very different plan for his life. Born in Nairobi and spending part of his early years in Kenya before moving to the United States, his path didn’t initially point toward acting. In fact, he studied business and had a more traditional career in mind.</p>
                    <p>That changed almost by accident. While in college, he took an acting class—not out of passion, but curiosity. Something about performing, stepping into different characters, and telling stories through emotion clicked instantly. It wasn’t just interesting—it felt right.</p>
                    <p>He made a decision that many would consider risky: he fully committed to acting. After training at the prestigious New York University Tisch School of the Arts, he began the long, difficult climb typical of most actors—auditions, rejections, small roles, and uncertainty.</p>
                    <p>His breakthrough came when he landed the role of Laurent in The Twilight Saga. The franchise had a massive global audience, and suddenly, he was on one of the biggest stages in modern entertainment. But he didn’t stop there. Instead of being defined by a single role, he expanded his portfolio—appearing in major productions like X-Men: First Class and series such as The Blacklist. Each role added depth to his career and proved his range as an actor.</p>
                    <p>What makes his story stand out is the shift—from uncertainty to clarity. Acting wasn’t always the plan, but once he discovered it, he pursued it with precision and discipline. Today, Edi Gathegi represents something powerful for many young Africans interested in film: global success is possible, even when the starting point feels far removed from Hollywood.</p>
                </div>
            </div>
        </section>

        <!-- Story List -->
        <div class="story-list">
            <!-- Black Coffee -->
            <article class="story-card">
                <img src="https://files.manuscdn.com/user_upload_by_module/session_file/310519663587410563/LkMCbcEJzGaskTxi.png" alt="Black Coffee">
                <div>
                    <span class="category-tag">Music & Resilience</span>
                    <h3>The DJ Who Took African Sound Global – Black Coffee</h3>
                    <p>Long before he became one of the most respected DJs in the world, Black Coffee was just a young man in South Africa with a deep love for music. His journey wasn’t easy. After an accident in his early twenties left him with partial paralysis in one arm, many would have seen it as a limitation—especially in a field that often demands physical precision and endurance.</p>
                    <p>But he didn’t see it that way. He adapted. Instead of stepping back, he focused on production—creating music that blended deep house with African rhythms. His sound was distinct, rooted in identity, and different from mainstream electronic music at the time. That difference became his advantage.</p>
                    <p>As his tracks gained attention, his reputation grew—not just locally, but internationally. He began performing at major global venues, including Ibiza, one of the world’s most iconic music destinations. Then came a defining moment. He won a Grammy Award for Best Dance/Electronic Album, becoming one of the few African DJs to achieve that level of recognition on the global stage.</p>
                    <p>But beyond awards, his impact runs deeper. Black Coffee helped reshape how African electronic music is perceived worldwide. He didn’t follow trends—he introduced his own sound and stayed consistent with it. Today, he stands as a symbol of resilience and originality. His story shows that setbacks don’t have to limit direction. With the right focus, they can redefine it.</p>
                </div>
            </article>

            <!-- Trending: AI Entertainment -->
            <article class="story-card">
                <img src="https://files.manuscdn.com/user_upload_by_module/session_file/310519663587410563/bpikolzsqMteCTYi.png" alt="AI Entertainment">
                <div>
                    <span class="category-tag">Future Tech</span>
                    <h3>The Big Takeover: How AI is Redefining the Cinematic Experience</h3>
                    <p>As we move further into 2026, the entertainment landscape is undergoing a seismic shift. AI-generated content is no longer a novelty; it's flooding social feeds, streaming platforms, and even cinema screens. From fully AI-produced 'microdramas' to personalized holographic experiences, the way we consume stories is changing forever. But as technology advances, the question remains: can an algorithm ever truly capture the human soul?</p>
                </div>
            </article>

            <!-- Trending: Sustainable Cities -->
            <article class="story-card">
                <img src="https://files.manuscdn.com/user_upload_by_module/session_file/310519663587410563/UQpOrxbisBPBQRYr.png" alt="Sustainable Cities">
                <div>
                    <span class="category-tag">Environment</span>
                    <h3>Green Horizons: Africa's Bold Leap into Sustainable Urbanism</h3>
                    <p>Across the continent, a new vision of the city is emerging. From Nairobi to Lagos, architects and urban planners are rejecting traditional extractive models in favor of vertical gardens, solar-integrated skyscrapers, and electric transit systems. These 'Green Cities' are not just about aesthetics; they represent a fundamental shift in how African nations are positioning themselves as leaders in the global fight against climate change.</p>
                </div>
            </article>
        </div>
    </main>

    <aside class="sidebar">
        <div class="sidebar-widget">
            <h3 class="widget-title">Trending Now</h3>
            <div class="trending-item">
                <img src="https://files.manuscdn.com/user_upload_by_module/session_file/310519663587410563/kXFDvRPFcIvMmWME.png" alt="African Fashion">
                <div>
                    <h4>Haute Couture: African Fashion Dominates Global Runways</h4>
                </div>
            </div>
            <div class="trending-item">
                <img src="https://files.manuscdn.com/user_upload_by_module/session_file/310519663587410563/bpikolzsqMteCTYi.png" alt="AI Tech">
                <div>
                    <h4>Vigloo Debuts First Fully AI-Produced Microdrama</h4>
                </div>
            </div>
            <div class="trending-item">
                <img src="https://files.manuscdn.com/user_upload_by_module/session_file/310519663587410563/UQpOrxbisBPBQRYr.png" alt="Green City">
                <div>
                    <h4>Lagos Ranks Top in Global Sustainable City Index</h4>
                </div>
            </div>
        </div>

        <div class="sidebar-widget">
            <h3 class="widget-title">The Rule Authority</h3>
            <p style="font-family: var(--font-body); font-size: 0.9rem; text-align: center; font-style: italic;">"Providing the definitive perspective on the stories that shape our world."</p>
        </div>

        <div class="sidebar-widget">
            <h3 class="widget-title">Follow The Rule</h3>
            <div style="display: flex; justify-content: center; gap: 25px; font-size: 1.8rem;">
                <i class="fab fa-facebook"></i>
                <i class="fab fa-twitter"></i>
                <i class="fab fa-instagram"></i>
                <i class="fab fa-linkedin"></i>
            </div>
        </div>
    </aside>
</div>

<footer>
    <div class="footer-inner">
        <div class="footer-social">
            <i class="fab fa-facebook"></i>
            <i class="fab fa-twitter"></i>
            <i class="fab fa-instagram"></i>
            <i class="fab fa-linkedin"></i>
            <i class="fab fa-youtube"></i>
        </div>
        <img src="https://files.manuscdn.com/user_upload_by_module/session_file/310519663587410563/YTcqjfynEoJTHdXH.png" alt="The Rule Logo" class="footer-logo">
        <div class="footer-links">
            <p class="footer-text">&copy; 2026 THE RULE. TRUTH & AUTHORITY. ALL RIGHTS RESERVED.</p>
            <a href="#" class="footer-tos">Terms of Service</a>
            <a href="#" class="footer-tos">Privacy Policy</a>
        </div>
    </div>
</footer>

</body>
</html>
