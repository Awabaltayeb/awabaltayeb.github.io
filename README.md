<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Awab Altayeb - CV</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #0d3b66;
            color: white;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #071a2f;
            padding: 10px;
            text-align: center;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            overflow-x: auto; /* لإضافة خاصية التحريك */
            white-space: nowrap; /* لجعل الروابط في سطر واحد */
        }

        nav ul {
            list-style-type: none;
            padding: 0;
            margin: 0;
            display: inline-block; /* تغيير طريقة العرض */
        }

        nav ul li {
            display: inline-block;
            margin-right: 20px;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-size: 18px;
            transition: color 0.3s ease;
        }

        nav ul li a:hover {
            color: #00aaff;
        }

        .about-section {
            text-align: center;
            padding: 50px;
            background-color: #071a2f;
            margin-top: 60px;
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }

        .about-section h1 {
            font-size: 36px;
        }

        .about-section p {
            font-size: 18px;
            color: #ccc;
            margin: 20px 0;
        }

        .about-section img {
            border-radius: 50%;
            width: 150px;
            height: 150px;
            margin-bottom: 20px;
        }

        .skills-section, .projects-section, .experience-section, .contact-section {
            padding: 50px;
            text-align: center;
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }

        .section-title {
            font-size: 32px;
            margin-bottom: 20px;
            color: #00aaff;
        }

        footer {
            background-color: #071a2f;
            text-align: center;
            padding: 20px;
            color: #ccc;
            margin-top: 50px;
        }

        /* Animation when hovering over titles */
        .section-title:hover {
            color: #00ff88;
            transition: color 0.5s ease;
        }

        /* Smooth scrolling */
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body>

    <header>
        <nav>
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section class="about-section" id="about">
        <img src="awabss.jpg" alt="Awab Altayeb">
        <h1>Awab Altayeb</h1>
        <p>Frontend Developer | Web Designer</p>
        <p>Thank you for visiting my website. I am here to provide innovative solutions in web design and development that enhance user experience and drive engagement.</p>
    </section>

    <section class="skills-section" id="skills">
        <h1 class="section-title">Skills</h1>
        <p>HTML, CSS, C++, Git, Visual Studio, Web Design, System Analysis and Design</p>
    </section>

    <section class="projects-section" id="projects">
        <h1 class="section-title">Projects</h1>
        <p>Designed an interactive webpage with enhanced user experience using HTML and CSS.</p>
    </section>

    <section class="experience-section" id="experience">
        <h1 class="section-title">Experience</h1>
        <p>Community Work: Organized and led agricultural projects and volunteer initiatives.</p>
    </section>

    <!-- Contact Section -->
    <section class="contact-section" id="contact">
        <h1 class="section-title">Contact</h1>
        <p>Phone: +24963268532</p>
        <p>Email: Awabaltayeb28@gmail.com</p>
        <p>Location: Al Jazirah State, Al Kamlin Locality</p>
    </section>

    <footer>
        <p>Created by Awab Altayeb © 2024</p>
    </footer>

    <script>
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();

                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Function to reveal sections when scrolling
        const sections = document.querySelectorAll('.about-section, .skills-section, .projects-section, .experience-section, .contact-section');

        window.addEventListener('scroll', reveal);

        function reveal() {
            let windowHeight = window.innerHeight;
            let windowTop = window.scrollY;

            sections.forEach(section => {
                let sectionTop = section.offsetTop;

                if (windowTop + windowHeight > sectionTop + 100) {
                    section.style.opacity = 1;
                    section.style.transform = 'translateY(0)';
                }
            });
        }
    </script>
</body>
</html>
