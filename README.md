<!DOCTYPE html -->
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>UCF DARKSTAR - EVE Frontier Gaming & Streaming</title>
    <link rel="stylesheet" href="favicon.ico" type="image/x-icon">
    <style>
        /* Global Styles */
        body {
            margin: 0;
            font-family: 'Roboto', sans-serif;
            background-color: #121212;
            color: #ffffff;
            color: #000000;
            line-height: 1.6;
        }

        /* Dark Theme */
        body.dark-theme {
            background-color: #121212;
            color: #e0e9e0;
        }

        /* Navbar */
        nav {
            background-color: #1f1f1f;
            padding: 1rem;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0, 0, 0,0.5);
        }

        nav ul {
            list-style: none;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
        }

        nav li {
            margin: 0 1rem;
        }

        nav a {
            color: #ffffff;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s;
        }

        nav a:hover {
            color: #ff4081;
        }

        /* Hero Section */
        .hero {
            background: url('https://via.placeholder.com/1920x800/121212/ffffff?text=EVE+Frontier+Universe') no-repeat center/cover;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: #ffffff;
        }

        .hero h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
        }

        .hero p {
            font-size: 1.5rem;
        }

        .hero button {
            background-color: #ff4081;
            border: none;
            padding: 1rem 2rem;
            color: #ffffff;
            font-size: 1.2rem;
            cursor: pointer;
            transition: background 0.3s;
        }

        .hero button:hover {
            background-color: #d81b60;
        }

        /* Sections */
        section {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        #about {
            background-color: #1e1f1f;
        }

        #streams {
            text-align: center;
        }

        .twitch-embed {
            margin: 2rem auto;
            width: 80%;
            height: 500px;
        }

        #gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
        }

        .gallery-item img {
            width: 100%;
            transition: transform 0.3s;
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        #contact form {
            display: flex;
            flex-direction: column;
            gap: 1rem;
            max-width: 500px;
            margin: 0 auto;
        }

        input, textarea {
            padding: 1rem;
            background-color: #333;
            border: 1px solid #444;
            color: #fff;
        }

        button[type="submit"] {
            background-color: #ff4081;
            border: none;
            padding: 1rem;
            color: pointer;
            cursor: pointer;
        }

        /* Footer */
        footer {
            background-color: #1f1f1f;
            padding: 1rem;
            text-align: center;
            position: relative;
            bottom: 0;
            width: 100%;
        }

        /* JS for interactivity */
        /* This will be in separate file, but inline for now */
        <script>
            // Simple section scrolling
            document.addEventListener('DOMContentLoaded', () => {
                const navLinks = document.querySelectorAll('nav a');
                navLinks.forEach(link => {
                    link.addEventListener('click', (e) => {
                        e.preventDefault();
                        const targetId = link.getAttribute('href').substring(1);
                        const target = document.getElementById(targetId');
                        if (target) {
                            target.scrollIntoView({
                                behavior: 'smooth'
                            });
                        }
                    });
                });

                // Form submission placeholder
                const form = document.querySelector('#contact form');
                form.addEventListener('submit', (e) => {
                    e.preventDefault();
                    alert('Form submitted! (Placeholder)');
                    form.reset();
                });

                // Gallery lightbox placeholder
                const galleryItems = document.querySelectorAll('.gallery-item');
                galleryItems.forEach(item => {
                    item.addEventListener('click', () => {
                        alert('Opening image in lightbox (placeholder)');
                    });
                });
            });
        </script>

        /* Media Queries for Responsiveness */
        @media (max-width: 768px) {
            nav ul {
                flex-direction: column;
            }

            nav li {
                margin: 0.5rem 0;
            }

            .hero h1 {
                font-size: 3rem;
            }

            .hero p {
                font-size: 1.2rem;
            }

            .twitch-embed {
                width: 100%;
            }
        }
    </style>
</head>
<body class="dark-theme">

    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#streams">Streams</a></li>
            <li><a href="#gallery">Gallery</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <section id="home" class="hero">
        <div>
            <h1>Welcome to UCF DARKSTAR</h1>
            <p>Your hub for EVE Frontier adventures and Twitch streams</p>
            <button onclick="document.getElementById('streams').scrollIntoView({behavior: 'smooth'})">Watch Live</button>
        </div>
    </section>

    <section id="about">
        <h2>About UCF DARKSTAR</h2>
        <p>I'm UCF DARKSTAR, a passionate player of EVE Frontier, the ultimate space exploration and combat game. I spend my time navigating the vast universe, engaging in epic battles, and building my fleet.</p>
        <p>When I'm not in-game, I stream my gameplay on Twitch, sharing tips, strategies, and live reactions with my community. Join me for thrilling sessions and let's conquer the frontier together!</p>
    </section>

    <section id="streams">
        <h2>Twitch Streams</h2>
        <p>Check out my latest streams on EVE Frontier. I stream regularly – tune in for live gameplay!</p>
        <div class="twitch-embed">
            <!-- Replace 'ucfdarkstar' with your actual Twitch username -->
            <iframe
                src="https://player.twitch.tv/?channel=ucfdarkstar&parent=yourwebsite.com"
                frameborder="0"
                allowfullscreen="true"
                scrolling="no"
                height="100%"
                width="100%">
            </iframe>
        </div>
        <p>Follow me on Twitch: <a href="https://www.twitch.tv/ucfdarkstar" style="color: #ff4081;">twitch.tv/ucfdarkstar</a></p>
    </section>

    <section id="gallery">
        <h2>Gallery</h2>
        <p>Screenshots and highlights from EVE Frontier</p>
        <div class="gallery-item"><img src="https://via.placeholder.com/400x300/121212/ffffff?text=EVE+Battle+1" alt="Battle 1"></div>
        <div class="gallery-item"><img src="https://via.placeholder.com/400x300/121212/ffffff?text=EVE+Exploration" alt="Exploration"></div>
        <div class="gallery-item"><img src="https://via.placeholder.com/400x300/121212/ffffff?text=EVE+Fleet" alt="Fleet"></div>
        <div class="gallery-item"><img src="https://via.placeholder.com/400x300/121212/ffffff?text=EVE+Battle+2" alt="Battle 2"></div>
    </section>

    <section id="contact">
        <h2>Contact Me</h2>
        <p>Get in touch for collaborations, questions, or just to say hi!</p>
        <form>
            <input type="text" placeholder="Your Name" required>
            <input type="email" placeholder="Your Email" required>
            <textarea placeholder="Your Message" rows="5" required></textarea>
            <button type="submit">Send Message</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2025 UCF DARKSTAR. All rights reserved.</p>
        <p>Built for EVE Frontier enthusiasts.</p>
    </footer>

</body>
</html>
