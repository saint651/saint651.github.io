<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>THE RULE | Truth & Stories</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700;900&family=Playfair+Display:wght@700;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --color-bg: #ffffff;
            --color-text: #1a1a1a;
            --color-accent: #e31e24; /* Kahawa Tungu Red */
            --color-border: #eeeeee;
            --font-main: 'Montserrat', sans-serif;
            --font-heading: 'Playfair Display', serif;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { background-color: var(--color-bg); color: var(--color-text); font-family: var(--font-main); line-height: 1.6; }

        /* Header & Logo */
        header { border-bottom: 4px solid var(--color-accent); padding: 20px 0; text-align: center; }
        .logo-container { max-width: 1200px; margin: 0 auto; display: flex; flex-direction: column; align-items: center; }
        .logo-img { height: 80px; margin-bottom: 10px; }
        .tagline { font-size: 0.8rem; text-transform: uppercase; letter-spacing: 3px; font-weight: 700; color: #666; }

        /* Navigation */
        nav { border-bottom: 1px solid var(--color-border); background: #fff; position: sticky; top: 0; z-index: 1000; }
        .nav-inner { max-width: 1200px; margin: 0 auto; display: flex; justify-content: center; gap: 30px; padding: 15px 0; }
        .nav-inner a { text-decoration: none; color: var(--color-text); font-weight: 700; font-size: 0.85rem; text-transform: uppercase; transition: color 0.3s; }
        .nav-inner a:hover { color: var(--color-accent); }

        /* Main Layout */
        .container { max-width: 1200px; margin: 40px auto; display: grid; grid-template-columns: 1fr 350px; gap: 40px; padding: 0 20px; }

        /* Featured Story */
        .featured-story { grid-column: 1 / -1; margin-bottom: 40px; border-bottom: 1px solid var(--color-border); padding-bottom: 40px; }
        .featured-grid { display: grid; grid-template-columns: 1.5fr 1fr; gap: 30px; }
        .featured-img { width: 100%; border-radius: 4px; }
        .featured-content h2 { font-family: var(--font-heading); font-size: 2.5rem; margin-bottom: 20px; line-height: 1.1; }
        .category-tag { background: var(--color-accent); color: #fff; padding: 4px 12px; font-size: 0.7rem; font-weight: 900; text-transform: uppercase; display: inline-block; margin-bottom: 15px; }

        /* Story Cards */
        .story-list { display: flex; flex-direction: column; gap: 40px; }
        .story-card { display: grid; grid-template-columns: 300px 1fr; gap: 25px; align-items: start; }
        .story-card img { width: 100%; height: 200px; object-fit: cover; border-radius: 4px; }
        .story-card h3 { font-family: var(--font-heading); font-size: 1.5rem; margin-bottom: 10px; line-height: 1.2; }
        .story-card p { color: #555; font-size: 0.95rem; }

        /* Sidebar */
        .sidebar-widget { margin-bottom: 40px; }
        .widget-title { border-left: 5px solid var(--color-accent); padding-left: 15px; font-weight: 900; text-transform: uppercase; margin-bottom: 20px; font-size: 1.1rem; }
        .trending-item { display: flex; gap: 15px; margin-bottom: 20px; padding-bottom: 15px; border-bottom: 1px solid var(--color-border); }
        .trending-item img { width: 80px; height: 80px; object-fit: cover; border-radius: 4px; }
        .trending-item h4 { font-size: 0.9rem; line-height: 1.3; }

        footer { background: #1a1a1a; color: #fff; padding: 60px 0; margin-top: 60px; text-align: center; }
        .footer-logo { height: 50px; filter: brightness(0) invert(1); margin-bottom: 20px; }

        @media (max-width: 900px) {
            .container { grid-template-columns: 1fr; }
            .featured-grid { grid-template-columns: 1fr; }
            .story-card { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>

<header>
    <div class="logo-container">
        <img src="https://files.manuscdn.com/user_upload_by_module/session_file/310519663587410563/ThFwrmoRMPZioBQf.png" alt="The Rule Logo" class="logo-img">
        <div class="tagline">Truth & Stories</div>
    </div>
</header>

<nav>
    <div class="nav-inner">
        <a href="#">Home</a>
        <a href="#">News</a>
        <a href="#">Business</a>
        <a href="#">Celebrity</a>
        <a href="#">Politics</a>
        <a href="#">Technology</a>
        <a href="#">Sports</a>
    </div>
</nav>

<div class="container">
    <main class="main-content">
        <!-- Featured Story -->
        <section class="featured-story">
            <div class="featured-grid">
                <img src="https://files.manuscdn.com/user_upload_by_module/session_file/310519663587410563/AElRgHvPgPhhIfFC.png" alt="Edi Gathegi" class="featured-img">
                <div class="featured-content">
                    <span class="category-tag">Celebrity</span>
                    <h2>From Mathare to Netflix – The Journey of Edi Gathegi</h2>
                    <p>Before he appeared on global screens, Edi Gathegi had a very different plan for his life. Born in Nairobi and spending part of his early years in Kenya before moving to the United States, his path didn’t initially point toward acting...</p>
                    <br>
                    <p>While in college, he took an acting class—not out of passion, but curiosity. Something about performing, stepping into different characters, and telling stories through emotion clicked instantly. It wasn’t just interesting—it felt right.</p>
                </div>
            </div>
        </section>

        <!-- Story List -->
        <div class="story-list">
            <article class="story-card">
                <img src="https://files.manuscdn.com/user_upload_by_module/session_file/310519663587410563/LkMCbcEJzGaskTxi.png" alt="Black Coffee">
                <div>
                    <span class="category-tag">Music</span>
                    <h3>The DJ Who Took African Sound Global – Black Coffee</h3>
                    <p>Long before he became one of the most respected DJs in the world, Black Coffee was just a young man in South Africa with a deep love for music. After an accident in his early twenties left him with partial paralysis in one arm, many would have seen it as a limitation...</p>
                </div>
            </article>

            <article class="story-card">
                <img src="https://files.manuscdn.com/user_upload_by_module/session_file/310519663587410563/AElRgHvPgPhhIfFC.png" alt="Edi Gathegi Success">
                <div>
                    <span class="category-tag">Entertainment</span>
                    <h3>Global Success is Possible: The Edi Gathegi Representation</h3>
                    <p>Today, Edi Gathegi represents something powerful for many young Africans interested in film: global success is possible, even when the starting point feels far removed from Hollywood. His story shows that setbacks don’t have to limit direction.</p>
                </div>
            </article>
        </div>
    </main>

    <aside class="sidebar">
        <div class="sidebar-widget">
            <h3 class="widget-title">Trending Now</h3>
            <div class="trending-item">
                <img src="https://files.manuscdn.com/user_upload_by_module/session_file/310519663587410563/LkMCbcEJzGaskTxi.png" alt="Black Coffee">
                <div>
                    <h4>Black Coffee Wins Grammy for Best Dance Album</h4>
                </div>
            </div>
            <div class="trending-item">
                <img src="https://files.manuscdn.com/user_upload_by_module/session_file/310519663587410563/AElRgHvPgPhhIfFC.png" alt="Edi Gathegi">
                <div>
                    <h4>Edi Gathegi's Breakthrough in The Twilight Saga</h4>
                </div>
            </div>
        </div>

        <div class="sidebar-widget">
            <h3 class="widget-title">Follow Us</h3>
            <div style="display: flex; gap: 15px; font-size: 1.5rem;">
                <i class="fab fa-facebook"></i>
                <i class="fab fa-twitter"></i>
                <i class="fab fa-instagram"></i>
                <i class="fab fa-youtube"></i>
            </div>
        </div>
    </aside>
</div>

<footer>
    <div class="logo-container">
        <img src="https://files.manuscdn.com/user_upload_by_module/session_file/310519663587410563/ThFwrmoRMPZioBQf.png" alt="The Rule Logo" class="footer-logo">
        <p>&copy; 2026 THE RULE. All Rights Reserved.</p>
    </div>
</footer>

</body>
</html>
