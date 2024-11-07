<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rishit Kapoor's Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f7f9fc;
            color: #333;
            line-height: 1.6;
        }
        header {
            background: #2d3436;
            color: #fff;
            padding: 20px;
            text-align: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        nav {
            display: flex;
            justify-content: center;
            gap: 20px;
        }
        nav a {
            color: #fff;
            text-decoration: none;
            font-weight: 600;
            transition: color 0.3s;
        }
        nav a:hover {
            color: #00cec9;
        }
        .hero {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 60px 20px;
            text-align: center;
        }
        .hero img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            margin-bottom: 20px;
        }
        .hero h1 {
            font-size: 2.5em;
            margin: 10px 0;
        }
        .hero p {
            max-width: 600px;
        }
        section {
            padding: 40px 20px;
            margin: auto;
            max-width: 800px;
        }
        .project, .certification {
            background: #ffffff;
            margin: 20px 0;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .project h3, .certification h3 {
            margin-bottom: 10px;
        }
        .contact-info {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .contact-info a {
            color: #00cec9;
            text-decoration: none;
        }
        footer {
            background: #2d3436;
            color: #fff;
            text-align: center;
            padding: 10px 0;
        }
    </style>
</head>
<body>

<header>
    <nav>
        <a href="https://rishitkapoor.me#about">About</a>
        <a href="https://rishitkapoor.me#projects">Projects</a>
        <a href="https://rishitkapoor.me#certifications">Certifications</a>
        <a href="https://rishitkapoor.me#skills">Skills</a>
        <a href="https://rishitkapoor.me#contact">Contact</a>
    </nav>
</header>

<div class="hero">
    <img src="./Rishit Kapoor's PortfolioNEWMAN_files/Photo Rishit 50 KB ABOVE.jpg" alt="Rishit Kapoor"> 
 
    <h1>Rishit Kapoor</h1>
    <p>A passionate technology and cybersecurity enthusiast with expertise in cloud solutions and programming.</p>
</div>

<section id="about">
    <h2>About Me</h2>
    <p>I am Rishit Kapoor, dedicated to advancing in the fields of technology, cybersecurity, and development. My projects and certifications showcase my commitment to learning and innovation.</p>
</section>

<section id="projects">
    <h2>Projects</h2>
    <div class="project">
        <h3>Medimate</h3>
        <p>An AI-based healthcare application that prioritizes medicine administration and patient observations using Voice-Directed Technology and AI.</p>
    </div>
    <div class="project">
        <h3>21 Days of Coding Event</h3>
        <p>Organized and coordinated a coding event involving interactive activities, quizzes, and community support.</p>
    </div>
    <div class="project">
        <h3>AI ChatBot</h3>
        <p>In this project, we created a dynamic multi-agent collaboration system using LangChain and OpenAI's GPT-4, designed to streamline complex workflows. The system leverages specialized agents (like Researcher, Coder, and Chart Generator) coordinated by a supervisor agent, which intelligently manages each task. From configuring libraries to initializing tools, this project showcases advanced AI-driven task management and decision-making capabilities in real-time collaboration.</p>
    </div>
</section>

<section id="certifications">
    <h2>Certifications</h2>
    <div class="certification">
        <h3>AWS Cloud with AI Workshop</h3>
        <a href="http://www.lwindia.com/" target="_blank">
            <img src="./Rishit Kapoor's PortfolioNEWMAN_files/Rishit Kapoor.pdf" alt="View Certificate" width="200">
        </a>
    </div>
    <div class="certification">
        <h3>Bootcamp Certificates from AWS, Google, and Devtown</h3>
        <a href="./Rishit Kapoor's PortfolioNEWMAN_files/rishit-kapoor-33b2b81b0_learnit-manipaluniversityjaipur-righteducation-activity-7172273826230202368-94Ax" target="_blank">
            <img src="./Rishit Kapoor's PortfolioNEWMAN_files/rishit-kapoor-33b2b81b0_learnit-manipaluniversityjaipur-righteducation-activity-7172273826230202368-94Ax" alt="View Certificates" width="200">
        </a>
    </div>
    <div class="certification">
        <h3>Hacks 8.0 Certification</h3>
        <a href="https://certificate.givemycertificate.com/c/addc742e-4e36-470f-9e1f-d6adc93487ec" target="_blank">
            <img src="" alt="View Certificate" width="200">
        </a>
    </div>
</section>

<section id="skills">
    <h2>Skills</h2>
    <ul>
        <li>Cybersecurity</li>
        <li>SQL</li>
        <li>C Programming</li>
        <li>Linux Command Line</li>
        <li>Frontend and Backend Development</li>
    </ul>
</section>

<section id="contact">
    <h2>Contact</h2>
    <div class="contact-info">
        <p>Email: <a href="mailto:rishitkpr@gmail.com">rishitkpr@gmail.com</a></p>
        <p>LinkedIn: <a href="https://www.linkedin.com/in/rishit-kapoor-33b2b81b0/">Rishit Kapoor</a></p>
    </div>
</section>

<footer>
    <p>© 2024 Rishit Kapoor. All rights reserved.</p>
</footer>

</body>
</html>
