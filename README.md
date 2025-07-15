<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>UCF DARKSTAR - Gaming Stream</title>
    <style>
        /* Reset and Global Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }

        body {
            background-color: #121212; /* Dark theme for gaming vibe */
            color: #ffffff;
            line-height: 1.6;
        }

        /* Header Section */
        header {
            background: linear-gradient(to right, #000000, #1a1a1a);
            padding: 20px;
            text-align: center;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
        }

        header h1 {
            font-size: 2.5em;
            text-transform: uppercase;
            letter-spacing: 2px;
            animation: glow 2s infinite alternate;
        }

        @keyframes glow {
            from { text-shadow: 0 0 5px #ff00ff, 0 0 10px #ff00ff; }
            to { text-shadow: 0 0 10px #00ffff, 0 0 20px #00ffff; }
        }

        nav ul {
            list-style: none;
            margin-top: 10px;
        }

        nav ul li {
            display: inline;
            margin: 0 15px;
        }

        nav ul li a {
            color: #ffffff;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s;
        }

        nav ul li a:hover {
            color: #ff00ff;
        }

        /* Hero Section with Stream Embed */
        #hero {
            background: url('https://via.placeholder.com/1920x1080?text=Gaming+Background') no-repeat center/cover;
            height: 80vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            position: relative;
        }

        #hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.6); /* Overlay for readability */
        }

        #hero h2 {
            font-size: 3em;
            z-index: 1;
            margin-bottom: 20px;
        }

        #stream-embed {
            width: 80%;
            max-width: 800px;
            height: 450px;
            border: 2px solid #ff00ff;
            border-radius: 10px;
            overflow: hidden;
            z-index: 1;
        }

        /* About Section */
        #about {
            padding: 50px 20px;
            text-align: center;
        }

        #about h2 {
            font-size: 2em;
            margin-bottom: 20px;
            color: #00ffff;
        }

        #about p {
            max-width: 800px;
            margin: 0 auto 20px;
        }

        /* Schedule Section */
        #schedule {
            padding: 50px 20px;
            background-color: #1a1a1a;
        }

        #schedule h2 {
            text-align: center;
            font-size: 2em;
            margin-bottom: 30px;
            color: #ff00ff;
        }

        .schedule-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .schedule-item {
            background: #222222;
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            transition: transform 0.3s;
        }

        .schedule-item:hover {
            transform: scale(1.05);
        }

        .schedule-item h3 {
            color: #00ffff;
            margin-bottom: 10px;
        }

        /* Social Links Section */
        #social {
            padding: 50px 20px;
            text-align: center;
        }

        #social h2 {
            font-size: 2em;
            margin-bottom: 20px;
            color: #ff00ff;
        }

        .social-icons {
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        .social-icons a {
            color: #ffffff;
            font-size: 2em;
            transition: color 0.3s;
        }

        .social-icons a:hover {
            color: #00ffff;
        }

        /* Footer */
        footer {
            background: #000000;
            padding: 20px;
            text-align: center;
            font-size: 0.8em;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            #hero {
                height: 60vh;
            }

            #stream-embed {
                width: 100%;
                height: 300px;
            }

            header h1 {
                font-size: 2em;
            }
        }

        /* JavaScript Enhancements */
        .hidden {
            display: none;
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <h1>UCF DARKSTAR Gaming Stream</h1>
        <nav>
            <ul>
                <li><a href="#hero">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#schedule">Schedule</a></li>
                <li><a href="#social">Social</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section with Stream Embed (Replace the iframe src with your actual stream URL, e.g., Twitch embed) -->
    <section id="hero">
        <h2>Welcome to UCF DARKSTAR</h2>
        <div id="stream-embed">
            <iframe src="https://player.twitch.tv/?channel=your_twitch_channel&parent=yourwebsite.com" frameborder="0" allowfullscreen="true" scrolling="no" height="100%" width="100%"></iframe>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <h2>About UCF DARKSTAR</h2>
        <p>UCF DARKSTAR is your go-to destination for epic gaming streams, featuring high-energy gameplay from a variety of titles including FPS, RPGs, and indie gems. Join me as I dive deep into the worlds of virtual worlds, share pro tips, and connect with the community.</p>
        <p>With years of gaming experience and a passion for sci-fi themes, UCF DARKSTAR brings a unique twist to streaming. Whether you're here for the laughs, the thrills, or the strategies, there's always something exciting happening!</p>
    </section>

    <!-- Schedule Section -->
    <section id="schedule">
        <h2>Stream Schedule</h2>
        <div class="schedule-grid">
            <div class="schedule-item">
                <h3>Monday - FPS Night</h3>
                <p>7 PM - 10 PM EST</p>
                <p>Playing Call of Duty and Valorant</p>
            </div>
            <div class="schedule-item">
                <h3>Wednesday - RPG Adventures</h3>
                <p>8 PM - 11 PM EST</p>
                <p>Exploring Elden Ring and Cyberpunk 2077</p>
            </div>
            <div class="schedule-item">
                <h3>Friday - Community Games</h3>
                <p>6 PM - 9 PM EST</p>
                <p>Viewer requests and multiplayer fun</p>
            </div>
            <div class="schedule-item">
                <h3>Sunday - Chill Streams</h3>
                <p>4 PM - 7 PM EST</p>
                <p>Indie games and chat sessions</p>
            </div>
        </div>
    </section>

    <!-- Social Links -->
    <section id="social">
        <h2>Connect with Me</h2>
        <div class="social-icons">
            <a href="https://twitch.tv/yourchannel" target="_blank">Twitch</a> <!-- Use Font Awesome or SVG for real icons -->
            <a href="https://youtube.com/yourchannel" target="_blank">YouTube</a>
            <a href="https://twitter.com/yourhandle" target="_blank">Twitter</a>
            <a href="https://discord.gg/yourserver" target="_blank">Discord</a>
            <a href="https://instagram.com/yourhandle" target="_blank">Instagram</a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2025 UCF DARKSTAR. All rights reserved. Built with passion and code.</p>
    </footer>

    <!-- JavaScript for Interactivity -->
    <script>
        // Simple Scroll Spy for Nav Highlighting
        const sections = document.querySelectorAll('section');
        const navLinks = document.querySelectorAll('nav a');

        window.addEventListener('scroll', () => {
            let current = '';

            sections.forEach(section => {
                const sectionTop = section.offsetTop - 50;
                if (pageYOffset >= sectionTop) {
                    current = section.getAttribute('id');
                }
            });

            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.href.includes(`#${current}`)) {
                    link.classList.add('active');
                }
            });
        });

        // Add active class style
        const style = document.createElement('style');
        style.innerHTML = `
            nav a.active {
                color: #00ffff;
                border-bottom: 2px solid #ff00ff;
            }
        `;
        document.head.appendChild(style);

        // Toggle schedule items (example interactivity)
        const scheduleItems = document.querySelectorAll('.schedule-item');
        scheduleItems.forEach(item => {
            item.addEventListener('click', () => {
                item.classList.toggle('active');
                // Could add more details here if needed
            });
        });
    </script>

</body>
</html>
