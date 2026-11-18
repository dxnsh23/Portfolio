# Ex01 Portfolio
## Date: 30.10.2026
## Dinesh Raghavendara S - 212224040078

## AIM
To create a Portfolio using HTML and CSS.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for introduction, about, projects, and contact details.

### STEP 5
Define global styles for fonts, colors, and layout.

### STEP 6
Style the header, navigation bar, and sections.

### STEP 7
Use Flexbox or CSS Grid for layout design.

### STEP 8
Add hover effects and transitions for interactivity.

### STEP 9
Add Images and Media.

### STEP 10
Use optimized images for a professional look.

### STEP 11
Open the HTML file in a browser to check layout and functionality.

### STEP 12
Fix styling issues and refine content placement.

### STEP 13
Deploy the Portfolio.

### STEP 14
Upload to GitHub Pages for free hosting.

## PROGRAM
```.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dinesh Raghavendara | Portfolio</title>

    <style>
        /* 1. GLOBAL STYLES */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        :root {
            --accent: #38bdf8;
            --black: #090b10;
            --card: #12151d;
            --white: #f5f5f5;
            --grey: #a4a7b0;
        }

        body {
            font-family: Arial, sans-serif;
            background: var(--black);
            color: var(--white);
            line-height: 1.7;
        }

        a {
            color: inherit;
            text-decoration: none;
        }

        .container {
            width: 88%;
            max-width: 1100px;
            margin: auto;
        }

        section {
            padding: 85px 0;
            scroll-margin-top: 80px;
        }

        .title {
            font-size: 34px;
            text-align: center;
            margin-bottom: 10px;
        }

        .title span {
            color: var(--accent);
        }

        .subtitle {
            text-align: center;
            color: var(--grey);
            margin-bottom: 40px;
        }

        /* 2. NAVIGATION BAR */
        header {
            background: rgba(9, 11, 16, 0.95);
            border-bottom: 1px solid #252832;
            position: sticky;
            top: 0;
            z-index: 10;
        }

        nav {
            min-height: 72px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 20px;
        }

        .logo {
            font-size: 25px;
            font-weight: bold;
            letter-spacing: 2px;
        }

        .logo span {
            color: var(--accent);
        }

        .nav-links {
            display: flex;
            gap: 24px;
            list-style: none;
        }

        .nav-links a {
            font-size: 14px;
            color: var(--grey);
            transition: 0.3s;
        }

        .nav-links a:hover {
            color: var(--accent);
        }

        /* 3. HERO SECTION */
        #home {
            min-height: 88vh;
            display: flex;
            align-items: center;
            background:
                radial-gradient(ellipse at 85% 45%,
                #12334a55, transparent 45%),
                var(--black);
        }

        .hero {
            display: grid;
            grid-template-columns: 1.2fr 0.8fr;
            align-items: center;
            gap: 45px;
        }

        .tag {
            display: inline-block;
            color: var(--accent);
            border: 1px solid #155e75;
            padding: 6px 14px;
            border-radius: 4px;
            font-size: 12px;
            letter-spacing: 2px;
            margin-bottom: 22px;
        }

        .hero h1 {
            font-size: clamp(42px, 6vw, 68px);
            line-height: 1.12;
            margin-bottom: 18px;
        }

        .hero h1 span {
            color: var(--accent);
        }

        .hero h3 {
            color: #d3d4da;
            font-size: 19px;
            margin-bottom: 14px;
        }

        .hero p {
            color: var(--grey);
            margin-bottom: 28px;
            max-width: 530px;
        }

        .buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 14px;
        }

        .btn {
            display: inline-block;
            padding: 12px 21px;
            border: 1px solid var(--accent);
            border-radius: 4px;
            font-size: 14px;
            font-weight: bold;
            transition: 0.3s;
        }

        .primary {
            background: var(--accent);
            color: white;
        }

        .outline {
            color: var(--white);
        }

        .btn:hover {
            background: white;
            color: var(--black);
            border-color: white;
            transform: translateY(-3px);
        }

        /* CSS-ONLY REACTOR ILLUSTRATION */
        .reactor {
            width: 270px;
            height: 270px;
            margin: auto;
            border-radius: 50%;
            border: 2px solid #38bdf860;
            display: flex;
            align-items: center;
            justify-content: center;
            background: radial-gradient(circle,
                #38bdf830, #15131a 60%, #090b10 72%);
            box-shadow: 0 0 50px #38bdf81c;
        }

        .reactor-inner {
            width: 155px;
            height: 155px;
            border: 8px solid #0e7490;
            outline: 2px solid #7dd3fc;
            outline-offset: 8px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 40px;
            font-weight: bold;
            background: radial-gradient(circle,
                #38bdf8 0%, #075985 45%, #10121a 75%);
            box-shadow: 0 0 30px #38bdf860;
        }

        .hero-note {
            text-align: center;
            color: var(--grey);
            font-size: 12px;
            letter-spacing: 3px;
            margin-top: 30px;
        }

        /* 4. ABOUT SECTION */
        #about {
            background: #0e1016;
        }

        .about-card {
            max-width: 850px;
            margin: auto;
            padding: 32px;
            background: var(--card);
            border: 1px solid #292c36;
            border-left: 3px solid var(--accent);
            border-radius: 8px;
        }

        .about-card p {
            color: var(--grey);
            margin-bottom: 16px;
        }

        .education {
            padding: 20px;
            margin-top: 22px;
            background: #0b0d12;
            border: 1px solid #292c36;
            border-radius: 6px;
        }

        .education h3 {
            font-size: 17px;
            margin-bottom: 5px;
        }

        .education p {
            margin: 0;
            font-size: 14px;
        }

        /* 5. SKILLS SECTION */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }

        .skill-card {
            padding: 25px 18px;
            background: var(--card);
            border: 1px solid #292c36;
            border-radius: 7px;
            transition: 0.3s;
        }

        .skill-card:hover {
            border-color: var(--accent);
            transform: translateY(-5px);
        }

        .skill-icon {
            font-size: 30px;
            margin-bottom: 12px;
        }

        .skill-card h3 {
            margin-bottom: 8px;
        }

        .skill-card p {
            color: var(--grey);
            font-size: 14px;
        }

        /* 6. PROJECTS SECTION */
        #projects {
            background: #0e1016;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 24px;
        }

        .project-card {
            background: var(--card);
            border: 1px solid #292c36;
            border-radius: 8px;
            overflow: hidden;
            transition: 0.3s;
        }

        .project-card:hover {
            transform: translateY(-6px);
            border-color: var(--accent);
        }

        .project-banner {
            height: 155px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg,
                #102f46, #171923);
            font-size: 48px;
            border-bottom: 1px solid #292c36;
        }

        .project-content {
            padding: 24px;
        }

        .project-content h3 {
            margin-bottom: 10px;
        }

        .project-content p {
            color: var(--grey);
            font-size: 14px;
            margin-bottom: 16px;
        }

        .tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 20px;
        }

        .tags span {
            font-size: 11px;
            padding: 4px 10px;
            color: #7dd3fc;
            background: #38bdf815;
            border: 1px solid #155e75;
            border-radius: 3px;
        }

        .project-link {
            display: inline-block;
            color: var(--accent);
            font-size: 14px;
            font-weight: bold;
        }

        .project-link:hover {
            color: white;
        }

        /* 7. CONTACT SECTION */
        .contact-card {
            max-width: 700px;
            margin: auto;
            padding: 35px;
            text-align: center;
            background: var(--card);
            border: 1px solid #292c36;
            border-radius: 8px;
        }

        .contact-card p {
            color: var(--grey);
            margin: 15px 0 25px;
        }

        .contact-links {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 12px;
        }

        .contact-link {
            padding: 10px 18px;
            border: 1px solid #424550;
            border-radius: 4px;
            font-size: 14px;
            transition: 0.3s;
        }

        .contact-link:hover {
            background: var(--accent);
            border-color: var(--accent);
        }

        /* 8. FOOTER */
        footer {
            padding: 24px;
            text-align: center;
            background: #07080c;
            border-top: 1px solid #252832;
            color: var(--grey);
            font-size: 13px;
        }

        footer span {
            color: var(--accent);
        }

        /* 9. RESPONSIVE DESIGN */
        @media (max-width: 800px) {
            .hero {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .hero p {
                margin-left: auto;
                margin-right: auto;
            }

            .buttons {
                justify-content: center;
            }

            .reactor {
                width: 220px;
                height: 220px;
            }

            .reactor-inner {
                width: 125px;
                height: 125px;
            }

            .skills-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .nav-links {
                gap: 12px;
            }
        }

        @media (max-width: 520px) {
            nav {
                flex-direction: column;
                padding: 12px 0;
                gap: 8px;
            }

            .nav-links {
                justify-content: center;
                flex-wrap: wrap;
                gap: 8px 14px;
            }

            .nav-links a {
                font-size: 12px;
            }

            .hero h1 {
                font-size: 40px;
            }

            .skills-grid,
            .projects-grid {
                grid-template-columns: 1fr;
            }

            .about-card,
            .contact-card {
                padding: 22px;
            }

            section {
                padding: 60px 0;
            }
        }
    </style>
</head>

<body>

    <!-- NAVIGATION -->
    <header>
        <nav class="container">
            <a href="#home" class="logo">DINESH<span> R</span></a>

            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- HOME SECTION -->
    <section id="home">
        <div class="container hero">

            <div>
                
                <h1>BUILDING<br>THE <span>FUTURE.</span></h1>

                <h3>Computer Science Student | Aspiring Innovator</h3>

                <p>
                    I am a CSE student passionate about artificial
                    intelligence, software development and solving
                    real-world problems through technology.
                    I believe great ideas deserve great execution.
                </p>

                <div class="buttons">
                    <a href="#projects" class="btn primary">
                        Explore Projects &#8599;
                    </a>

                    <a href="#contact" class="btn outline">
                        Contact Me &#8599;
                    </a>
                </div>
            </div>

            <div>
                <div class="reactor">
                    <div class="reactor-inner">DR</div>
                </div>
                <p class="hero-note">INTELLIGENCE. INNOVATION. IMPACT.</p>
            </div>

        </div>
    </section>

    <!-- ABOUT SECTION -->
    <section id="about">
        <div class="container">
            <h2 class="title">ABOUT <span>ME</span></h2>
            <p class="subtitle">The person behind the projects.</p>

            <div class="about-card">
                <p>
                    Hello! I am Dinesh Raghavendara, a Computer Science and
                    Engineering student at Saveetha Engineering College.
                </p>

                <p>
                    I enjoy programming, exploring artificial
                    intelligence and building projects that combine
                    logical thinking with practical applications.
                </p>

                <p>
                    My goal is to keep learning, develop innovative
                    solutions and pursue opportunities in advanced
                    technology and research.
                </p>

                <div class="education">
                    <h3>&#127891; Education</h3>
                    <p>B.Tech - Computer Science and Engineering</p>
                    <p>Saveetha Engineering College</p>
                    <p>2024 - 2028</p>
                </div>
            </div>
        </div>
    </section>

    <!-- SKILLS SECTION -->
    <section id="skills">
        <div class="container">
            <h2 class="title">MY <span>ARSENAL</span></h2>
            <p class="subtitle">Tools I use to turn ideas into reality.</p>

            <div class="skills-grid">

                <div class="skill-card">
                    <div class="skill-icon">&#128013;</div>
                    <h3>Python</h3>
                    <p>Programming, automation and machine learning.</p>
                </div>

                <div class="skill-card">
                    <div class="skill-icon">&#128187;</div>
                    <h3>Web Development</h3>
                    <p>HTML, CSS and responsive web design.</p>
                </div>

                <div class="skill-card">
                    <div class="skill-icon">&#129302;</div>
                    <h3>Artificial Intelligence</h3>
                    <p>Exploring intelligent models and applications.</p>
                </div>

                <div class="skill-card">
                    <div class="skill-icon">&#128451;</div>
                    <h3>Database Systems</h3>
                    <p>SQL, data organization and database concepts.</p>
                </div>

                <div class="skill-card">
                    <div class="skill-icon">&#9749;</div>
                    <h3>Java</h3>
                    <p>Object-oriented programming and problem-solving.</p>
                </div>

                <div class="skill-card">
                    <div class="skill-icon">&#9889;</div>
                    <h3>Critical Thinking</h3>
                    <p>Logical reasoning and algorithmic thinking.</p>
                </div>

            </div>
        </div>
    </section>

    <!-- PROJECTS SECTION -->
    <section id="projects">
        <div class="container">
            <h2 class="title">FEATURED <span>PROJECTS</span></h2>
            <p class="subtitle">Ideas engineered into working solutions.</p>

            <div class="projects-grid">

                <div class="project-card">
                    <div class="project-banner">&#129504;</div>

                    <div class="project-content">
                        <h3>Skin Disease Prediction</h3>

                        <p>
                            An AI-based project exploring image
                            classification to identify skin disease
                            categories and provide educational
                            information about them.
                        </p>

                        <div class="tags">
                            <span>Python</span>
                            <span>TensorFlow</span>
                            <span>AI / ML</span>
                        </div>

                        <a href="https://github.com/"
                           target="_blank"
                           rel="noopener noreferrer"
                           class="project-link">
                            View Source &#8599;
                        </a>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-banner">&#128421;</div>

                    <div class="project-content">
                        <h3>My Portfolio</h3>

                        <p>
                            A personal website showcasing my
                            background, technical skills, projects
                            and professional interests.
                        </p>

                        <div class="tags">
                            <span>HTML</span>
                            <span>CSS</span>
                            <span>Responsive Design</span>
                        </div>

                        <a href="#home" class="project-link">
                            Back to Home &#8599;
                        </a>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-banner">&#128200;</div>

                    <div class="project-content">
                        <h3>Data Analytics</h3>

                        <p>
                            A project area for exploring datasets,
                            discovering patterns and presenting
                            useful insights through visualizations.
                        </p>

                        <div class="tags">
                            <span>Python</span>
                            <span>Pandas</span>
                            <span>Data Science</span>
                        </div>

                        <a href="https://github.com/"
                           target="_blank"
                           rel="noopener noreferrer"
                           class="project-link">
                            View Source &#8599;
                        </a>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-banner">&#128640;</div>

                    <div class="project-content">
                        <h3>Future Innovation</h3>

                        <p>
                            A space for my upcoming experiments,
                            creative ideas and new technology
                            projects.
                        </p>

                        <div class="tags">
                            <span>Research</span>
                            <span>Innovation</span>
                            <span>Development</span>
                        </div>

                        <a href="#contact" class="project-link">
                            Discuss a Project &#8599;
                        </a>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- CONTACT SECTION -->
    <section id="contact">
        <div class="container">
            <h2 class="title">LET'S <span>CONNECT</span></h2>
            <p class="subtitle">Every great collaboration starts somewhere.</p>

            <div class="contact-card">
                <h3>Have an idea? Let's build it.</h3>

                <p>
                    I am interested in technology, collaborative
                    projects, research and opportunities to learn.
                    Feel free to reach out.
                </p>

                <div class="contact-links">
                    <a href="mailto:your-email@example.com"
                       class="contact-link">
                        &#9993; Email
                    </a>

                    <a href="https://github.com/"
                       target="_blank"
                       rel="noopener noreferrer"
                       class="contact-link">
                        GitHub &#8599;
                    </a>

                    <a href="https://www.linkedin.com/"
                       target="_blank"
                       rel="noopener noreferrer"
                       class="contact-link">
                        LinkedIn &#8599;
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <p>
            Designed and built by <span>Dinesh Raghavendara</span> |
            &#169; 2026 All Rights Reserved.
        </p>
        <p>ENGINEER YOUR OWN FUTURE.</p>
        <p><a href="#home">Back to Top &#8593;</a></p>
    </footer>

</body>
</html>

```

## OUTPUT
<img width="1600" height="894" alt="image" src="https://github.com/user-attachments/assets/77eca357-bbf8-44e9-88ef-147aa0316464" />



## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
