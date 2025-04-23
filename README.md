<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tickle My Funny Bone</title>
    <link href="https://fonts.googleapis.com/css2?family=Comic+Neue:wght@700&family=Roboto:wght@400&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            line-height: 1.6;
            color: #222;
            background: linear-gradient(135deg, #ffeb3b, #ff5722);
            overflow-x: hidden;
        }

        nav {
            background: #d81b60;
            color: white;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 5px rgba(0,0,0,0.3);
        }

        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            padding: 1.2rem 0;
        }

        nav ul li {
            margin: 0 2rem;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-family: 'Comic Neue', cursive;
            font-size: 1.2rem;
            text-transform: uppercase;
            transition: color 0.3s;
        }

        nav ul li a:hover {
            color: #ffeb3b;
        }

        section {
            min-height: 100vh;
            padding: 6rem 2rem;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            font-family: 'Roboto', sans-serif;
        }

        #home {
            background: rgba(255, 255, 255, 0.9);
            border-radius: 20px;
            margin: 2rem;
            max-width: 900px;
            animation: slideIn 1s ease-out;
        }

        #about {
            background: rgba(255, 235, 59, 0.8);
            border-radius: 20px;
            margin: 2rem;
            max-width: 900px;
        }

        #projects {
            
            background: repeating-linear-gradient(
        45deg,
        #f0f0f0,
        #f0f0f0 10px,
        #e0e0e0 10px,
        #e0e0e0 20px
    );
            border-radius: 20px;
            margin: 2rem;
            max-width: 900px;
        }

        #contact {
            background: rgba(255, 235, 59, 0.8);
            border-radius: 20px;
            margin: 2rem;
            max-width: 900px;
        }

        h1 {
            font-family: 'Comic Neue', cursive;
            font-size: 3.5rem;
            color: #d81b60;
            margin-bottom: 1.5rem;
            text-shadow: 2px 2px #ffeb3b;
        }

        .tickle-heading {
            display: inline-block;
            animation: bounceAndRotate 2s infinite;
        }

        h2 {
            font-family: 'Comic Neue', cursive;
            font-size: 2.5rem;
            color: #222;
            margin-bottom: 1rem;
        }

        p {
            max-width: 700px;
            font-size: 1.1rem;
            margin-bottom: 1.5rem;
            color: #333;
        }

        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            max-width: 1000px;
            width: 100%;
        }

        .project-card {
            background: #fff;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
            transition: transform 0.3s, box-shadow 0.3s;
            border: 2px solid #ff5722;
        }

        .project-card:hover {
            transform: scale(1.05);
            box-shadow: 0 6px 15px rgba(0,0,0,0.3);
        }

        .project-card h3 {
            font-family: 'Comic Neue', cursive;
            color: #d81b60;
            margin-bottom: 0.5rem;
        }

        .contact-links {
            display: flex;
            gap: 1.5rem;
            margin-top: 1rem;
        }

        .contact-links a {
            color: #ff5722;
            text-decoration: none;
            font-family: 'Comic Neue', cursive;
            font-size: 1.2rem;
            transition: color 0.3s;
        }

        .contact-links a:hover {
            color: #d81b60;
        }

        /* Cartoon Character Styles */
        .cartoon-character {
            width: 100px;
            height: 100px;
            margin-bottom: 1rem;
        }

        #home .cartoon-character {
            animation: wave 3s infinite;
        }

        #about .cartoon-character {
            animation: blink 4s infinite;
        }

        #projects .cartoon-character {
            animation: bounce 2s infinite;
        }

        #contact .cartoon-character {
            animation: spin 5s infinite linear;
        }

        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes bounceAndRotate {
            0%, 100% {
                transform: translateY(0) rotate(0deg);
            }
            25% {
                transform: translateY(-15px) rotate(5deg);
            }
            50% {
                transform: translateY(0) rotate(0deg);
            }
            75% {
                transform: translateY(-15px) rotate(-5deg);
            }
        }

        @keyframes wave {
            0%, 100% {
                transform: rotate(0deg);
            }
            50% {
                transform: rotate(20deg);
            }
        }

        @keyframes blink {
            0%, 10%, 100% {
                transform: scaleY(1);
            }
            5% {
                transform: scaleY(0.1);
            }
        }

        @keyframes bounce {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-10px);
            }
        }

        @keyframes spin {
            0% {
                transform: rotate(0deg);
            }
            100% {
                transform: rotate(360deg);
            }
        }

        @media (max-width: 768px) {
            nav ul {
                flex-direction: column;
                align-items: center;
            }

            nav ul li {
                margin: 0.8rem 0;
            }

            h1 {
                font-size: 2.5rem;
            }

            h2 {
                font-size: 2rem;
            }

            section {
                padding: 4rem 1rem;
                margin: 1rem;
            }

            .cartoon-character {
                width: 80px;
                height: 80px;
            }
        }
    </style>
</head>
<body>
    <nav>
        <ul>
            <li><a href="#home">Laugh Central</a></li>
            <li><a href="#about">Wit Wizard</a></li>
            <li><a href="#projects">Giggle Works</a></li>
            <li><a href="#contact">Poke Me</a></li>
        </ul>
    </nav>

    <section id="home">
        <!-- Jester Character -->
        <svg class="cartoon-character" viewBox="0 0 100 100">
            <circle cx="50" cy="50" r="40" fill="#ffeb3b" stroke="#d81b60" stroke-width="3"/>
            <circle cx="35" cy="40" r="5" fill="#222"/>
            <circle cx="65" cy="40" r="5" fill="#222"/>
            <path d="M35 60 Q50 70 65 60" fill="none" stroke="#222" stroke-width="3"/>
            <path d="M20 20 L10 10 M80 20 L90 10 M50 10 L50 0" fill="none" stroke="#d81b60" stroke-width="3"/>
        </svg>
        <h1><span class="tickle-heading">Tickle My Funny Bone</span></h1>
        <p>Welcome to the lair of KayYes, where satire and humor collide to roast life's absurdities. Buckle up for a wild ride!</p>
    </section>

    <section id="about">
        <!-- Philosopher Character -->
        <svg class="cartoon-character" viewBox="0 0 100 100">
            <rect x="30" y="30" width="40" height="40" fill="#ff5722" stroke="#222" stroke-width="3"/>
            <circle cx="40" cy="40" r="4" fill="#222"/>
            <circle cx="60" cy="40" r="4" fill="#222"/>
            <path d="M40 55 Q50 60 60 55" fill="none" stroke="#222" stroke-width="3"/>
            <path d="M30 70 L30 90 M70 70 L70 90" fill="none" stroke="#222" stroke-width="3"/>
        </svg>
        <h2>About the Chief Jester</h2>
        <p>I'm KayYes, a word-slinger who turns life's nonsense into laugh-out-loud satire. From mocking corporate jargon to skewering social media clowns, I wield humor like a sword. My mission? To make you snort coffee out your nose.</p>
    </section>

    <section id="projects">
        <svg class="cartoon-character" viewBox="0 0 100 100">
            <path d="M10 50 C 30 10 70 10 90 50" fill="none" stroke="#f4511e" stroke-width="5" stroke-linecap="round"/>
            <path d="M10 50 C 30 90 70 90 90 50" fill="none" stroke="#d81b60" stroke-width="5" stroke-linecap="round"/>
        </svg>
        <h2>Giggle Works: The Anticipation Build-Up (Mostly My Procrastination)</h2>
        <p>The comedic masterpieces of tomorrow are currently in their intensive "thinking about it" phase. Prepare for future hilarity... once I actually, you know, create it.</p>
        </section>

    <section id="contact">
        <!-- Hippo Character -->
        <svg class="cartoon-character" viewBox="0 0 100 100">
            <ellipse cx="50" cy="60" rx="40" ry="30" fill="#d81b60" stroke="#222" stroke-width="3"/>
            <circle cx="40" cy="40" r="4" fill="#222"/>
            <circle cx="60" cy="40" r="4" fill="#222"/>
            <path d="M40 50 Q50 55 60 50" fill="none" stroke="#222" stroke-width="3"/>
            <rect x="45" y="70" width="10" height="10" fill="#fff"/>
        </svg>
        <h2>Throw Me a Bone</h2>
        <p>Got a ridiculous idea or want to collaborate on a satirical masterpiece? Holler at me!</p>
        <div class="contact-links">
            <a href="mailto:pkshenoy@gmail.com">Email</a>
        </div>
    </section>

    <script>
        // Smooth scrolling for nav links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Add a fun hover effect on project cards
        document.querySelectorAll('.project-card').forEach(card => {
            card.addEventListener('mouseover', () => {
                card.style.background = '#ffeb3b';
            });
            card.addEventListener('mouseout', () => {
                card.style.background = '#fff';
            });
        });
    </script>
</body>
</html>
