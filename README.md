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

        /* RESET: Essential to remove all white gaps and ensure full width */
        html, body {
            margin: 0;
            padding: 0;
            width: 100%;
            background-color: var(--color-bg);
            overflow-x: hidden; /* Prevent horizontal scroll */
        }

        * { box-sizing: border-box; }
        
        body { 
            color: var(--color-text); 
            font-family: var(--font-main); 
            line-height: 1.6;
            -webkit-text-size-adjust: 100%; /* Prevent text scaling issues on mobile */
        }

        header { border-bottom: 4px solid var(--color-accent); padding: 30px 0; text-align: center; }
        .logo-container { max-width: 1200px; margin: 0 auto; display: flex; flex-direction: column; align-items: center; padding: 0 20px; }
        .logo-img { max-width: 100%; height: auto; max-height: 180px; margin-bottom: 10px; }
        .tagline { font-size: 0.9rem; text-transform: uppercase; letter-spacing: 5px; font-weight: 700; color: #333; margin-top: -10px; }

        nav { border-bottom: 1px solid var(--color-border); background: #fff; position: sticky; top: 0; z-index: 1000; }
        .nav-inner { max-width: 1200px; margin: 0 auto; display: flex; justify-content: center; gap: 20px; padding: 15px 10px; flex-wrap: wrap; }
        .nav-inner a { text-decoration: none; color: var(--color-text); font-weight: 700; font-size: 0.8rem; text-transform: uppercase; transition: color 0.3s; }
        .nav-inner a:hover { color: var(--color-accent); }

        /* FIXED: Container width and padding to prevent text cutoff */
        .container { 
            max-width: 1200px; 
            margin: 40px auto; 
            display: grid; 
            grid-template-columns: 1fr 350px; 
            gap: 40px; 
            padding: 0 20px; 
            width: 100%;
        }

        .featured-story { grid-column: 1 / -1; margin-bottom: 40px; border-bottom: 2px solid #000; padding-bottom: 40px; }
        .featured-grid { display: grid; grid-template-columns: 1.5fr 1fr; gap: 40px; }
        
        /* FIXED: Image scaling - No cropping, no oversized images */
        .featured-img { 
            width: 100%; 
            height: auto; 
            max-height: 500px; /* Prevent oversized images */
            display: block;
            border-radius: 0; 
            box-shadow: 10px 10px 0px var(--color-accent); 
            object-fit: contain; /* Ensure whole image is seen */
            background: #f9f9f9;
        }
        
        .featured-content h2 { font-family: var(--font-heading); font-size: clamp(2rem, 5vw, 3rem); margin-bottom: 20px; line-height: 1.1; font-weight: 900; }
        .featured-content p { font-family: var(--font-body); font-size: 1.1rem; color: #333; margin-bottom: 15px; word-wrap: break-word; }
        .category-tag { background: var(--color-accent); color: #fff; padding: 4px 12px; font-size: 0.75rem; font-weight: 900; text-transform: uppercase; display: inline-block; margin-bottom: 15px; }

        .story-list { display: flex; flex-direction: column; gap: 50px; }
        .story-card { display: grid; grid-template-columns: 350px 1fr; gap: 30px; align-items: start; border-bottom: 1px solid var(--color-border); padding-bottom: 30px; }
        
        /* FIXED: Story card image scaling */
        .story-card img { 
            width: 100%; 
            height: auto; 
            max-height: 300px; /* Prevent oversized images */
            display: block;
            object-fit: contain; /* Ensure whole image is seen */
            background: #f9f9f9;
        }
        
        .story-card h3 { font-family: var(--font-heading); font-size: clamp(1.5rem, 4vw, 1.8rem); margin-bottom: 15px; line-height: 1.2; }
        .story-card p { font-family: var(--font-body); color: #444; font-size: 1rem; word-wrap: break-word; }

        .sidebar-widget { margin-bottom: 50px; background: #f9f9f9; padding: 20px; border-top: 3px solid #000; }
        .widget-title { font-weight: 900; text-transform: uppercase; margin-bottom: 25px; font-size: 1.2rem; letter-spacing: 1px; text-align: center; border-bottom: 1px solid #ddd; padding-bottom: 10px; }
        .trending-item { display: flex; gap: 15px; margin-bottom: 20px; padding-bottom: 15px; border-bottom: 1px solid #eee; }
        .trending-item:last-child { border-bottom: none; }
        .trending-item img { width: 90px; height: 90px; object-fit: cover; flex-shrink: 0; }
        .trending-item h4 { font-size: 0.95rem; line-height: 1.3; font-family: var(--font-heading); }

        /* TUKO STYLE FOOTER: Full-width dark green/black block */
        footer { 
            background: #004d2c; /* Tuko's signature dark green */
            color: #fff; 
            padding: 60px 0 0 0; 
            margin-top: 80px; 
            width: 100%; 
            display: block;
            border-top: 1px solid #003d23;
        }
        .footer-inner {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            text-align: left;
        }
        .footer-column h3 {
            font-size: 1rem;
            text-transform: uppercase;
            margin-bottom: 20px;
            border-bottom: 1px solid rgba(255,255,255,0.1);
            padding-bottom: 10px;
            letter-spacing: 1px;
        }
        .footer-column ul {
            list-style: none;
            padding: 0;
        }
        .footer-column ul li {
            margin-bottom: 10px;
        }
        .footer-column ul li a {
            color: rgba(255,255,255,0.7);
            text-decoration: none;
            font-size: 0.9rem;
            transition: color 0.3s;
        }
        .footer-column ul li a:hover {
            color: #fff;
        }
        
        .footer-bottom {
            background: #003d23; /* Darker bottom bar */
            padding: 30px 0;
            margin-top: 60px;
            width: 100%;
        }
        .footer-bottom-inner {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 20px;
        }
        .footer-copyright {
            font-size: 0.85rem;
            color: rgba(255,255,255,0.6);
        }
        .footer-social-icons {
            display: flex;
            gap: 20px;
            font-size: 1.2rem;
        }
        .footer-social-icons a {
            color: #fff;
            opacity: 0.8;
            transition: opacity 0.3s;
        }
        .footer-social-icons a:hover {
            opacity: 1;
        }

        /* RESPONSIVE FIXES: Ensure readability on all screens */
        @media (max-width: 900px) {
            .container { grid-template-columns: 1fr; padding: 0 15px; }
            .featured-grid { grid-template-columns: 1fr; gap: 20px; }
            .story-card { grid-template-columns: 1fr; gap: 20px; }
            .footer-bottom-inner { justify-content: center; text-align: center; flex-direction: column; }
            .logo-img { max-height: 120px; }
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
        <div class="footer-column">
            <h3>About Our Company</h3>
            <ul>
                <li><a href="#">About Us</a></li>
                <li><a href="#">Our Authors</a></li>
                <li><a href="#">Contact Us</a></li>
                <li><a href="#">Our Manifesto</a></li>
                <li><a href="#">Advertise with us</a></li>
            </ul>
        </div>
        <div class="footer-column">
            <h3>Legal</h3>
            <ul>
                <li><a href="#">Privacy policy</a></li>
                <li><a href="#">Terms and conditions</a></li>
                <li><a href="#">Policies and standards</a></li>
                <li><a href="#">Cookie policy</a></li>
                <li><a href="#">DMCA removal</a></li>
            </ul>
        </div>
        <div class="footer-column">
            <h3>Social Media</h3>
            <ul>
                <li><a href="#">Facebook</a></li>
                <li><a href="#">Instagram</a></li>
                <li><a href="#">YouTube</a></li>
                <li><a href="#">X (Twitter)</a></li>
                <li><a href="#">LinkedIn</a></li>
            </ul>
        </div>
    </div>
    <div class="footer-bottom">
        <div class="footer-bottom-inner">
            <div class="footer-copyright">
                THE RULE MEDIA LTD, 2026<br>
                All rights reserved
            </div>
            <div class="footer-social-icons">
                <a href="#"><i class="fab fa-facebook"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="fab fa-youtube"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-linkedin"></i></a>
            </div>
        </div>
    </div>
</footer>

</body>
</html>
