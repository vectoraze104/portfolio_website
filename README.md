<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Project Landing Page</title>
    
    <!-- Bootstrap CSS -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css">
    
    <!-- FontAwesome Icons -->
    <script src="https://kit.fontawesome.com/f34207a9b4.js" crossorigin="anonymous"></script>

    <!-- Particle.js -->
    <script src="https://cdn.jsdelivr.net/particles.js/2.0.0/particles.min.js"></script>

    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Roboto+Slab:wght@100;300;400;700&display=swap" rel="stylesheet">

    <!-- Maps Leaflet CSS -->
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css" />


    
    <style>
/* ===== GENERAL STYLES ===== */
body {
    font-family: 'Roboto Slab', serif;
}

/* ===== FULL-SCREEN SECTION STYLING ===== */
.section {
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
}

/* ===== BACKGROUND ANIMATION ===== */
#particles-js {
    position: absolute;
    width: 100%;
    height: 100vh;
    background: #1d2620;
    z-index: -1;
    top: 0;
    left: 0;
}

/* ===== NAVIGATION BAR ===== */

.navbar {
    padding: 5px 10px;  /* Reduce padding */
    min-height: 50px;   /* Reduce navbar height */
    background: #334240;
}

.navbar-brand {
    font-family: 'Roboto Slab', serif;
    font-size: 1.5rem;
    font-weight: 700;
    color: #17a2b8;
}

.navbar-nav {
    margin-left: auto;
}
/* Ensure sections align properly when scrolled */
section {
    scroll-margin-top: 20px; /* Adjust for navbar height */
}

.nav-link {
    font-family: 'Roboto Slab', serif;
    font-size: 1rem;
    font-weight: 350;
    color: #efefef;
}

.nav-link:hover {
    color: #17a2b8;
}
/* Active Navigation Link */
.nav-link.active {
    font-weight: bold;
    color: #17a2b8 !important; /* Highlight color */
    border-bottom: 2px solid #17a2b8; /* Underline effect */
    transition: all 0.3s ease-in-out;
}

/* ===== LANDING PAGE ===== */
.landing-container {
    height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
}

.description {
    font-size: 1.2rem;
    font-weight: 500;
    color: #b4b4b4;
    text-align: center;
    margin-top: 80px;
    margin-bottom: 2px;
}

/* ===== CAROUSEL TEXT SECTION ===== */
.text-carousel-container {
    text-align: center;
    max-width: 600px;
    margin: 0 auto;
    height: 50px;
    position: relative;
    overflow: hidden;
    margin-top: 20px;
}

#carousel-text {
    font-size: 1.4rem;
    font-weight: 280;
    color: #bababa;
    font-family: "Roboto Slab", serif;
    margin-top: 50px;
    transition: opacity 0.5s ease-in-out;
}

/* ===== NAME & LOGO ===== */
.name-logo {
    display: flex;
    align-items: center;
    font-size: 3rem;
    font-weight: bold;
    color: #efefef;
    margin-top: 200px;
}

.name-logo img {
    width: 70px;
    height: 70px;
    margin: 10px;
}

/* ===== SOCIAL ICONS ===== */
.social-icons {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin-top: 15px;
}

.social-icons a {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background-color: #474747;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: 0.3s;
    text-decoration: none;
}

.social-icons a i {
    font-size: 24px;
    color: white;
}

.social-icons a:hover {
    background-color: #17a2b8;
}

/* ===== SCROLL DOWN ARROW ===== */
.scroll-down {
    position: absolute;
    bottom: 10px;
    left: 50%;
    transform: translateX(-50%);
    font-size: 2rem;
    color: #17a2b8;
    transition: 0.3s;
}

.scroll-down:hover {
    color: orange;
}

/* ===== ABOUT ME SECTION ===== */
.about-section {
    height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background-color: #f8f9fa;
    padding: 5%;
    margin-bottom: 100px;
}

.about-container {
    display: flex;
    max-width: 1200px;
    width: 100%;
    align-items: center;
    justify-content: space-between;
    gap: 50px;
}

/* About Me Image */
.about-image {
    max-width: 300px;
    height: auto;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

/* About Me Text */
.about-text {
    font-family: "Roboto Slab", serif;
    font-weight: 320;
    font-size: 1.2rem;
    color: #333;
    text-align: justify;
}

/* About Buttons */
.about-buttons a {
    display: inline-block;
    padding: 10px 15px;
    border: 1px solid #17a2b8;
    color: #17a2b8;
    text-decoration: none;
    font-size: 1rem;
    margin: 10px;
    border-radius: 5px;
    transition: 0.3s;
}

.about-buttons a:hover {
    background: #17a2b8;
    color: white;
}

/* ===== TIMELINE IMAGE STYLING ===== */
.timeline-image-container {
    margin-top: 90px;
    text-align: center;
    width: 100%;
}

.timeline-image {
    max-width: 100%;
    max-height: auto;
    border-radius: 10px;
    display: block;
    margin: 0 auto;
}

/* ===== EXPERIENCE SECTION STYLING ===== */
.experience-section {
    background-color: #f8f9fa;
    padding: 80px 0;
    text-align: center;
}

.experience-tabs {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 20px;
    margin-bottom: 20px;
}

.exp-tab {
    font-size: 1rem;
    font-weight: 500;
    color: #333;
    cursor: pointer;
    transition: color 0.3s ease-in-out;
}

.exp-tab:hover {
    color: #007bff;
}

.exp-tab.active {
    color: #007bff;
    border-bottom: 2px solid #007bff;
    padding-bottom: 5px;
}

/* Experience Content Box */
.experience-content {
    max-width: 800px;
    margin: 0 auto;
    background: white;
    padding: 30px;
    border-radius: 10px;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
    text-align: left;
}

/* Hide all experience details initially */
.exp-detail {
    display: none;
}

.exp-detail.active {
    display: block;
}

/* Experience Text Formatting */
.exp-company {
    color: #007bff;
    text-decoration: none;
    font-weight: 600;
}

.exp-duration {
    font-size: 1rem;
    color: #6c757d;
    font-weight: 500;
    margin-bottom: 10px;
}

.exp-list {
    padding-left: 20px;
}

.exp-list li {
    margin-bottom: 8px;
}

/* ===== EDUCATION SECTION STYLING ===== */
.education-section {
    background-color: #f8f9fa;
    padding: 80px 0;
    margin-top: 200px;
    text-align: center;
}

.education-card {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 800px;
    margin: 20px auto;
    background: white;
    padding: 20px;
    border-radius: 12px;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease-in-out;
}

.education-card:hover {
    transform: translateY(-5px);
}

.education-info {
    text-align: left;
    flex-grow: 1;
}

.education-info h3 {
    font-size: 1.2rem;
    font-weight: 600;
    color: #333;
    margin-bottom: 5px;
}

.edu-institution {
    color: #007bff;
    text-decoration: none;
    font-weight: 500;
}

.edu-institution:hover {
    text-decoration: underline;
}

.edu-details {
    font-size: 0.9rem;
    color: #6c757d;
    margin-top: 5px;
}

.education-year {
    font-size: 1rem;
    font-weight: 500;
    color: #333;
    white-space: nowrap;
}



/* ===== project SECTION (UPDATED) ===== */
.project-section {
    height: 950px;
    padding-top: 80px;
    padding-bottom: 50px;
    text-align: center;
    background-color: #1d2620;
}

/* project Grid */
.project-section .row {
    margin-top: 20px;
    justify-content: center;
}

/* project Title */
#project .section-title {
    font-size: 2rem;
    font-weight: 700;
    margin-bottom: 10px;
    color: #efefef;
}

/* Subtext */
.project-subtext {
    font-size: 1.2rem;
    font-weight: 300;
    margin-bottom: 30px;
    color: #8a8a8a;
}

/* project Items Grid */
.project-item {
    position: relative;
    overflow: hidden;
    border-radius: 10px;
    display: block;
    transition: transform 0.3s ease-in-out;
}

/* project Images */
.project-item img {
    width: 100%;
    height: 250px;
    object-fit: cover;
    border-radius: 10px;
    transition: transform 0.5s ease-in-out; /* Adjust speed here */
}

/* Hover Effect */
.project-item:hover img {
    transform: scale(1.05);
    opacity: 0.8;
}

/* project Overlay */
.project-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(9, 58, 43, 0.6);
    color: white;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    opacity: 0;
    transition: 1s;
    border-radius: 10px;
}

.project-item:hover .project-overlay {
    opacity: 1;
}

/* Overlay Text */
.project-overlay h3 {
    font-size: 1.5rem;
    font-weight: 700;
}

.project-overlay p {
    font-size: 1rem;
    font-weight: 300;
}

/* ===== CERTIFICATIONS SECTION STYLING ===== */
.certifications-section {
    background-color: #f8f9fa;
    padding: 80px 0;
    text-align: center;
    overflow: hidden;
    white-space: nowrap;
    position: relative;
    margin-top: 50px;
}

/* Scrolling container */
.certifications-slider {
    display: flex;
    overflow: hidden;
    position: relative;
    width: 100%;
    margin-top: 100px;
}

/* Moving images */
.certifications-track {
    display: flex;
    gap: 40px; /* Increased gap for better spacing */
    animation: scroll 80s linear infinite;
}

/* Certification images - Increased size by 40% */
.certification-image {
    max-width: 610px; /* Previously 150px (150 * 1.4 = 210) */
    max-height: 440px; /* Previously 100px (100 * 1.4 = 140) */
    object-fit: contain;
    border-radius: 5px;
}

/* Smooth infinite scrolling effect */
@keyframes scroll {
    from {
        transform: translateX(0%);
    }
    to {
        transform: translateX(-100%);
    }
}

/* ===== CONTACT SECTION ===== */
.contact-section {
    padding: 50px 0;
    background-color: #f8f9fa;
    margin-top: 60px;
    margin-bottom: 80px;
}

#contact .section-title {
    font-size: 2rem;
    font-weight: 500;
    color: black;
}
/* Contact Subtext */
.contact-subtext {
    font-family: "Roboto Slab", serif;
    font-size: 1rem;
    font-weight: 300;
    color: #545b61; /* Subtle gray color */
    margin-bottom: 20px;
    line-height: 1.6;
}
/* Contact Buttons */
.contact-buttons {
    display: flex;
    justify-content: center;
    gap: 15px;
    margin-top: 20px;
}

.contact-buttons a {
    display: inline-block;
    padding: 10px 20px;
    border: 1px solid #17a2b8;
    color: #17a2b8;
    text-decoration: none;
    font-size: 0.9rem;
    border-radius: 5px;
    transition: all 0.3s ease-in-out;
}

.contact-buttons a:hover {
    background: #17a2b8;
    color: white;
    transform: scale(1.1); /* Slight zoom effect on hover */
}


/* ===== MAP SECTION ===== */
#map-section {
    width: 100%;
    height: 300px;
    margin-top: 40px;
}

#map {
    width: 100%;
    height: 100%;
    border-radius: 10px;
}

/* ===== MODAL ===== */
.modal-content {
    max-width: 800px;
    margin: auto;
    padding: 20px;
    border-radius: 10px;
}

.modal-content img {
    width: 100%;
    max-height: 300px;
    object-fit: cover;
    display: block;
    margin: 0 auto 20px;
    border-radius: 10px;
}


    </style>
</head>
<body>

<!-- Background Animation -->
<div id="particles-js"></div>

<!-- Navigation -->
<nav class="navbar navbar-expand-lg navbar-light fixed-top">
    <div class="container">
        <a class="navbar-brand" href="#">HOME</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav ms-auto"> <!-- Centers the navbar items -->
                <li class="nav-item"><a class="nav-link" href="#about">About Me</a></li>
                <li class="nav-item"><a class="nav-link" href="#experience">Experience</a></li>
                <li class="nav-item"><a class="nav-link" href="#education">Education</a></li>
                <li class="nav-item"><a class="nav-link" href="#project">Projects</a></li>
                <li class="nav-item"><a class="nav-link" href="#certifications">Certifications</a></li>
                <li class="nav-item"><a class="nav-link" href="#contact">Contact</a></li>
                <li class="nav-item">
                    <a class="nav-link" href="Tanay_Singh_Resume.pdf" target="_blank" rel="noopener noreferrer">Resume</a>
                </li>
            </ul>
        </div>
    </div>
</nav>




<!-- Landing Page -->
<div class="landing-container section">
    <div class="name-logo">
        <span>TANAY</span>
        <img src="icons/Home_single_big_1.png" alt="Logo">
        <span>SINGH</span>
    </div>
    <div class="name-underline"></div>

    <div class="social-icons">
        <a href="https://www.github.com/vectoraze104" target="_blank"><i class="fa-brands fa-github"></i></a>
        <a href="https://www.linkedin.com/in/tanay-singh" target="_blank"><i class="fa-brands fa-linkedin-in"></i></a>
        <a href="https://www.hackerrank.com/profile/tanay_singh2013" target="_blank"><i class="fa-brands fa-hackerrank"></i></a>
        <a href="https://www.leetcode.com/u/vectoraze/" target="_blank"><i class="fa-solid fa-l"></i></a>
    </div>

    <!-- Main Headline (Stays Static) -->
<!-- Main Headline (Stays Static) -->
<p class="description">👋 Hi! I'm a Data Scientist specializing in <strong>SQL, Python </strong>&<strong> data visualization.</strong></p>

<!-- Text Carousel -->
<p id="carousel-text" class="carousel-animation">Transforming Data into Powerful Visual Stories</p>


    <a href="#about" class="scroll-down">
        <i class="fa-solid fa-chevron-down"></i>
    </a>
</div>

<!-- About Me Section -->
<section id="about" class="about-section">
    <div class="container">
        <div class="row align-items-center">
            <!-- Left Column: Profile Image -->
            <div class="col-md-4 text-center">
                <img src="images/about/personal.jpeg" alt="My Photo" class="about-image">
            </div>

            <!-- Right Column: About Me Text -->
            <div class="col-md-8">
                <h2 class="section-title">Hi, I'm Tanay.</h2>
                <p class="about-text">
                    I specialize in helping companies and researchers analyze and visualize their datasets. 
                    I excel in <strong>data visualization</strong>. If you're looking for guidance on presenting 
                    your results or building complex interactive charts, I'm the expert you're seeking.
                </p>
                <p class="about-text">
                    With a solid track record in data science, I've collaborated with top research institutes 
                    and leading private companies. My expertise spans various technologies, bridging the gap 
                    between <strong>design and functionality</strong>.
                </p>

                <!-- Buttons -->
                <div class="about-buttons">
                    <a href="#project" class="scroll-link">Projects</a>

                    <a href="https://leetcode.com/u/vectoraze/">LeetCode</a>
                    <a href="https://www.hackerrank.com/profile/tanay_singh2013">HackerRank</a>
                    <a href="https://github.com/vectoraze104">GitHub</a>
                </div>

                <!-- Timeline Image Placeholder -->
                <div class="timeline-image-container">
                    <img src="images/about/timeline.png" alt="Experience Timeline" class="timeline-image">
                </div>
            </div>
        </div>
    </div>
</section>

<!-- Experience Section -->
<section id="experience" class="experience-section">
    <div class="container">
        <h2 class="section-title">Experience</h2>

        <!-- Experience Tabs -->
        <div class="experience-tabs">
            <span class="exp-tab active" data-target="exp-northeastern">Northeastern University</span>
            <span class="exp-tab" data-target="exp-montal">MontAI</span>
            <span class="exp-tab" data-target="exp-legato">Legato</span>
            <span class="exp-tab" data-target="exp-middleeast">Middle East Management Consultancy</span>
            <span class="exp-tab" data-target="exp-manipal">Manipal Institute of Technology</span>
            <span class="exp-tab" data-target="exp-cgi">CGI</span>
        </div>

        <!-- Experience Content -->
        <div class="experience-content">
            <!-- Northeastern University -->
            <div class="exp-detail active" id="exp-northeastern">
                <h3>Data Engineer | Data Analyst - <a href="#" class="exp-company">Northeastern University</a></h3>
                <p class="exp-duration">Feb 2023 - Sep 2023</p>
                <ul class="exp-list">
                    <li>Engineered high-availability data streaming analytics platform, ensuring a <b>98%</b> real-time uptime for <b>20</b> smart homes using Python.</li>
                    <li>Built an energy dashboard visualizing Key Performance Indicators (<b>KPIs</b>) and metrics using <b>SQL, MariaDB</b>, and <b>Jupyter Notebooks</b>.</li>
                    <li>Applied SQL query optimization and software engineering best practices, leading to a <b>60%</b> reduction in SQL query response times.</li>
                    <li>Performed in-depth Exploratory Data Analysis (<b>EDA</b>) to unveil patterns and trends to support data-driven decision-making processes.</li>
                </ul>
            </div>

            <!-- MontAI -->
            <div class="exp-detail" id="exp-montal">
                <h3>AI Research Intern - <a href="#" class="exp-company">MontAI</a></h3>
                <p class="exp-duration">Jul 2022 - Dec 2022</p>
                <ul class="exp-list">
                    <li>Developed deep learning models to enhance chatbot intelligence using NLP and TensorFlow.</li>
                    <li>Collaborated with a research team to optimize AI models, reducing processing time by <b>35%</b>.</li>
                </ul>
            </div>

            <!-- Legato -->
            <div class="exp-detail" id="exp-legato">
                <h3>Software Engineer - <a href="#" class="exp-company">Legato</a></h3>
                <p class="exp-duration">Jan 2021 - Jun 2022</p>
                <ul class="exp-list">
                    <li>Designed scalable microservices architecture using AWS and Kubernetes.</li>
                    <li>Implemented CI/CD pipelines, reducing deployment time by <b>50%</b>.</li>
                </ul>
            </div>

            <!-- Middle East Management Consultancy -->
            <div class="exp-detail" id="exp-middleeast">
                <h3>Business Intelligence Analyst - <a href="#" class="exp-company">Middle East Management Consultancy</a></h3>
                <p class="exp-duration">Mar 2020 - Dec 2020</p>
                <ul class="exp-list">
                    <li>Developed data visualization dashboards to track financial performance.</li>
                    <li>Integrated machine learning models for predictive analytics.</li>
                </ul>
            </div>

            <!-- Manipal Institute of Technology -->
            <div class="exp-detail" id="exp-manipal">
                <h3>Practice School Student | Researcher - <a href="#" class="exp-company">Manipal Institute of Technology</a></h3>
                <p class="exp-duration">Jan 2016 - May 2016</p>
                <ul class="exp-list">
                    <li>Developed a Central Data Repository for MIT, Manipal.</li>
                    <li>Built a web application for data entry, analysis, and report generation.</li>
                    <li>Utilized <b>Sqoop</b> and <b>Hadoop</b> for big data processing.</li>
                    <li>Generated dynamic reports using <b>Hive</b>.</li>
                </ul>
            </div>

            <!-- CGI -->
            <div class="exp-detail" id="exp-cgi">
                <h3>Software Development Intern - <a href="#" class="exp-company">CGI</a></h3>
                <p class="exp-duration">May 2015 - Jul 2015</p>
                <p>Developed a Project Management web application that enabled collaboration between users across departments.</p>
            </div>
        </div>
    </div>
</section>

<!-- Education Section -->
<section id="education" class="education-section">
    <div class="container">
        <h2 class="section-title">Education</h2>

        <!-- Education Cards -->
        <div class="education-card">
            <div class="education-info">
                <h3>Master of Science in Data Science</h3>
                <a href="https://www.ljmu.ac.uk/" class="edu-institution">Liverpool John Moore University, Liverpool, England, UK</a>
                <p class="edu-details">Relevant Coursework: Data Mining, Machine Learning, Machine Learning Operations, Natural Language Processing</p>
            </div>
            <div class="education-year">Aug 2021 - Feb 2023</div>
        </div>

        <div class="education-card">
            <div class="education-info">
                <h3>Executive Post-Graduate in Data Science</h3>
                <a href="https://www.iiitb.ac.in/" class="edu-institution">International Institute of Information Technology</a>
                <p class="edu-details">Relevant Coursework: Data Mining, Machine Learning, Machine Learning Operations, Data Visualization</p>
            </div>
            <div class="education-year">Aug 2021 - Nov 2022</div>
        </div>

        <div class="education-card">
            <div class="education-info">
                <h3>Master of Business Administration (MBA) – Marketing</h3>
                <a href="https://www.siu.edu.in/" class="edu-institution">Symbiosis International University</a>
                <p class="edu-details">Relevant Coursework: Marketing Techniques, Business Administration</p>
            </div>
            <div class="education-year">May 2016 - Apr 2018</div>
        </div>

        <div class="education-card">
            <div class="education-info">
                <h3>Bachelor of Sciences – Business Administration</h3>
                <class="edu-institution">IHM Pusa
            </div>
            <div class="education-year">May 2012 - Apr 2015</div>
        </div>
    </div>
</section>



<!-- project Section -->
<section id="project" class="project-section">
    <div class="container">
        <!-- project Title & Subtext -->
        <h2 class="section-title">PROJECTS</h2>
        <p class="project-subtext">A glimpse of the projects I've been working on</p>
        <!-- project Grid (3x3 Structure) -->
        <div class="container">
            <div class="row g-4"> <!-- g-4 adds spacing between columns -->

                <!-- Project 1 -->
                <div class="col-md-4">
                    <a href="#" class="project-item" data-bs-toggle="modal" data-bs-target="#projectModal"
                       data-title="Bike Sharing Demand Analytics"
                       data-description="Assessing the impact of weather on bikesharing in San Francisco."
                       data-image="images/portfolio/sfo.jpg"
                       data-category="python">
                        <img src="images/portfolio/sfo.jpg" alt="Project 1">
                        <div class="project-overlay">
                            <h3>Bike Sharing Demand Analytics</h3>
                            <p>Assessing the impact of weather on bikesharing in San Francisco.</p>
                        </div>
                    </a>
                </div>

                <!-- Project 2 -->
                <div class="col-md-4">
                    <a href="#" class="project-item" data-bs-toggle="modal" data-bs-target="#projectModal"
                       data-title="All Things SQL"
                       data-description="SQL solutions for various website questions."
                       data-image="images/portfolio/scraper.jpg"
                       data-category="sql">
                        <img src="images/portfolio/sql.png" alt="Project 2">
                        <div class="project-overlay">
                            <h3>All Things SQL</h3>
                            <p>SQL solutions for various website questions.</p>
                        </div>
                    </a>
                </div>

                <!-- Project 3 -->
                <div class="col-md-4">
                    <a href="#" class="project-item" data-bs-toggle="modal" data-bs-target="#projectModal"
                       data-title="YouTube Sentiment Analysis"
                       data-description="Creating an NLP Model with Python to find the sentiments for a movie from its trailer."
                       data-image="images/portfolio/output.jpg"
                       data-category="scientific">
                        <img src="images/portfolio/youtube_1.jpg" alt="Project 3">
                        <div class="project-overlay">
                            <h3>YouTube Sentiment Analysis</h3>
                            <p>Creating an NLP Model with Python to find the sentiments for a movie from its trailer.</p>
                        </div>
                    </a>
                </div>

                <!-- Project 4 -->
                <div class="col-md-4">
                    <a href="https://github.com/vectoraze104/webscraper" class="project-item" data-bs-toggle="modal" data-bs-target="#projectModal"
                       data-title="WebScraper"
                       data-description="Scraping and analyzing web data using Python."
                       data-image="images/portfolio/output.jpg"
                       data-category="data-engineering">
                        <img src="images/portfolio/output.jpg" alt="Project 4">
                        <div class="project-overlay">
                            <h3>WebScraper</h3>
                            <p>Scraping and analyzing web data using Python.</p>
                        </div>
                    </a>
                </div>

                <!-- Project 5 -->
                <div class="col-md-4">
                    <a href="#" class="project-item" data-bs-toggle="modal" data-bs-target="#projectModal"
                       data-title="Predictive Analytics"
                       data-description="Using ML algorithms to predict real estate prices."
                       data-image="images/portfolio/machine-learning.jpg"
                       data-category="machine-learning">
                        <img src="images/portfolio/machine-learning.jpg" alt="Project 5">
                        <div class="project-overlay">
                            <h3>Predictive Analytics</h3>
                            <p>Using ML algorithms to predict real estate prices.</p>
                        </div>
                    </a>
                </div>

                <!-- Project 6 -->
                <div class="col-md-4">
                    <a href="#" class="project-item" data-bs-toggle="modal" data-bs-target="#projectModal"
                       data-title="Credit Card Fraud Analytics"
                       data-description="Running a fraud detection model on credit card transactions."
                       data-image="images/portfolio/cards.jpg"
                       data-category="python">
                        <img src="images/portfolio/cards.jpg" alt="Project 6">
                        <div class="project-overlay">
                            <h3>Credit Card Fraud Analytics</h3>
                            <p>Running a fraud detection model on credit card transactions.</p>
                        </div>
                    </a>
                </div>

            </div> <!-- End Row -->
        </div> <!-- End Container -->
    </div>
</section>
</section>

<!-- Certification Section -->
<section id="certifications" class="certifications-section">
    <h2 class="section-title">Certifications</h2>

    <div class="certifications-slider">
        <div class="certifications-track">
            <!-- Original Image Set -->
            <img src="images/certificates/applied_datascience_capstone.png" class="certification-image" alt="Certification 1">
            <img src="images/certificates/data_analysis_with_python.png" class="certification-image" alt="Certification 2">
            <img src="images/certificates/IBM_datascience.png" class="certification-image" alt="Certification 3">
            <img src="images/certificates/sql_advance.png" class="certification-image" alt="Certification 4">
            <img src="images/certificates/python_basic.png" class="certification-image" alt="Certification 5">
            <img src="images/certificates/python_badge_hackerrank.jpg" class="certification-image" alt="Certification 6">
            <img src="images/certificates/sql_badge_hackerrank.jpg" class="certification-image" alt="Certification 7">
            
            <!-- Duplicate Image Set for Seamless Loop -->
            <img src="images/certificates/applied_datascience_capstone.png" class="certification-image" alt="Certification 1">
            <img src="images/certificates/data_analysis_with_python.png" class="certification-image" alt="Certification 2">
            <img src="images/certificates/IBM_datascience.png" class="certification-image" alt="Certification 3">
            <img src="images/certificates/sql_advance.png" class="certification-image" alt="Certification 4">
            <img src="images/certificates/python_basic.png" class="certification-image" alt="Certification 5">
            <img src="images/certificates/python_badge_hackerrank.jpg" class="certification-image" alt="Certification 6">
            <img src="images/certificates/sql_badge_hackerrank.jpg" class="certification-image" alt="Certification 7">
        </div>
    </div>
</section>




<!-- Contact Me Section -->
<section id="contact" class="contact-section">
    <div class="container text-center">
        <h2 class="section-title">CONTACT</h2>
        <p class="contact-subtext">
            Feel free to contact me for any questions. <br>
            For open-source projects, please check my work on <a href="https://www.github.com/vectoraze104" target="_blank">GitHub</a> 
            and my professional profile on <a href="https://www.linkedin.com/in/tanay-singh" target="_blank">LinkedIn</a>. <br>
            You can also reach me via phone on <a href="tel:+14373229396">+1 (437) 322-9396</a> or email me at <a href="mailto:tanay.singh2013@gmail.com">tanay.singh2013@gmail.com</a>.
        </p>

        <!-- Contact Buttons -->
        <div class="contact-buttons">
            <a href="https://github.com/vectoraze104" target="_blank" class="btn btn-outline-info">GITHUB</a>
            <a href="tel:+14373229396" class="btn btn-outline-info">PHONE</a>
            <a href="mailto:tanay.singh2013@gmail.com" class="btn btn-outline-info">EMAIL</a>
            <a href="https://www.linkedin.com/in/tanay-singh" target="_blank" class="btn btn-outline-info">LINKEDIN</a> <!-- Replace LINKEDIN_PLACEHOLDER with your LinkedIn link -->
        </div>
    </div>
</section>

<!-- Map Section -->
<section id="map-section">
    <div id="map"></div>
</section>

<!-- Modal Structure -->
<div class="modal fade" id="projectModal" tabindex="-1" aria-labelledby="projectModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-lg">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title" id="projectModalLabel">Project Title</h5>
                <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
            </div>
            <div class="modal-body text-center">
                <img id="projectImage" src="" alt="Project Image" class="img-fluid">
                <p id="projectDescription" class="mt-3">Project description goes here...</p>
            </div>
            <div class="modal-footer">
                <a id="projectLink" href="#" target="_blank" class="btn btn-primary">View Project</a>
                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
            </div>
        </div>
    </div>
</div>


<script>
// Smooth Scroll for Down Arrow
document.querySelector('.scroll-down').addEventListener('click', function(e) {
    e.preventDefault();
    document.querySelector('#about').scrollIntoView({ behavior: 'smooth' });
});


// JavaScript to Handle Modal Data
document.addEventListener("DOMContentLoaded", function () {
    const projectItems = document.querySelectorAll(".project-item");

    projectItems.forEach(item => {
        item.addEventListener("click", function () {
            // Get data attributes
            const title = this.getAttribute("data-title");
            const description = this.getAttribute("data-description");
            const image = this.getAttribute("data-image");
            const link = this.getAttribute("data-link");

            // Populate modal with the data
            document.getElementById("projectModalLabel").textContent = title;
            document.getElementById("projectDescription").textContent = description;
            document.getElementById("projectImage").src = image;
            document.getElementById("projectLink").href = link;
        });
    });
});

// Smooth Scrolling for Navigation Links
document.querySelectorAll('.nav-link').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const targetId = this.getAttribute('href').substring(1);
        const targetSection = document.getElementById(targetId);
        window.scrollTo({
            top: targetSection.offsetTop - 10, // Adjusted for navbar height
            behavior: 'smooth'
        });
    });
});


// Highlight Navigation Links and Ensure Proper Content Scroll Alignment
document.addEventListener("scroll", function () {
    const sections = document.querySelectorAll("section");
    const navLinks = document.querySelectorAll(".nav-link");

    let currentSection = "";

    sections.forEach((section) => {
        const sectionTop = section.offsetTop - 160; // Offset to detect early
        const sectionHeight = section.clientHeight;

        if (window.scrollY >= sectionTop && window.scrollY < sectionTop + sectionHeight) {
            currentSection = section.getAttribute("id");
            section.classList.add("active-section"); // Highlight section content
        } else {
            section.classList.remove("active-section");
        }
    });

    navLinks.forEach((link) => {
        link.classList.remove("active");
        if (link.getAttribute("href").substring(1) === currentSection) {
            link.classList.add("active");
        }
    });
});



// Text Carousel Functionality
document.addEventListener("DOMContentLoaded", function () {
    const carouselTexts = [
        "Crafting Insightful Visualizations, One Dataset at a Time",
        "Making Data Speak Through Stunning Visuals",
        "Empowering Businesses with Interactive Data Solutions",
        "Data Visualization Expert | Turning Complexity into Clarity",
        "From Raw Data to Remarkable Dashboards",
        "Engineering Visuals That Drive Decision-Making",
        "Building Interactive Visualizations for a Data-Driven World",
        "Bridging the Gap Between Data and Design",
        "Where Code Meets Creativity in Data Science",
        "Pixels & Patterns: Crafting Data Stories That Matter",
        "Bringing Data to Life, One Visualization at a Time",
        "The Art of Data Storytelling Through Code",
        "Analyzing. Visualizing. Revolutionizing.",
        "Turning Complex Numbers into Simple Narratives"
    ];

    let index = 0;
    const carouselElement = document.getElementById("carousel-text");

    function updateCarousel() {
        carouselElement.style.opacity = 0; // Fade out effect
        setTimeout(() => {
            carouselElement.innerText = carouselTexts[index]; 
            carouselElement.style.opacity = 1; // Fade in effect
            index = (index + 1) % carouselTexts.length; // Loop back
        }, 500); 
    }

    setInterval(updateCarousel, 4000); // Change text every 4 seconds
});


    
</script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>

<!-- Maps Leaflet JS -->
<script src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js"></script>
<script>
    // Initialize the map
    var map = L.map('map').setView([43.65107, -79.347015], 10); // Toronto Coordinates

// Light Themed Map with Highlighted Streets
L.tileLayer('https://{s}.basemaps.cartocdn.com/light_all/{z}/{x}/{y}{r}.png', {
    attribution: '&copy; OpenStreetMap contributors &copy; CARTO',
    subdomains: 'abcd',
    maxZoom: 20
}).addTo(map);


    // Add a Marker for Toronto, ON
    L.marker([43.65107, -79.347015]).addTo(map)
        .bindPopup("<b>Tanay's Location</b><br>Toronto, ON")
        .openPopup();
</script>

<!-- Particle.js Configuration -->
<script>
    particlesJS("particles-js", {
        "particles": {
            "number": {
                "value": 120, /* Initial particle count */
                "density": { "enable": true, "value_area": 1000 }
            },
            "color": { "value": "#17a2b8" }, /* Change to your theme color */
            "shape": {
                "type": "triangle",
                "stroke": { "width": 0, "color": "#000000" },
                "polygon": { "nb_sides": 5 }
            },
            "opacity": {
                "value": 0.8, /* Make particles glow */
                "random": true,
                "anim": { "enable": true, "speed": 1, "opacity_min": 0.3, "sync": false }
            },
            "size": {
                "value": 4,
                "random": true,
                "anim": { "enable": true, "speed": 5, "size_min": 0.2, "sync": false }
            },
            "move": {
                "enable": true,
                "speed": 2,
                "direction": "none",
                "random": true,
                "straight": false,
                "out_mode": "out",
                "bounce": false
            },
            "line_linked": {
                "enable": true,
                "distance": 200,
                "color": "#17a2b8",
                "opacity": 0.6,
                "width": 1
            }
        },
        "interactivity": {
            "detect_on": "canvas",
            "events": {
                "onhover": { "enable": true, "mode": "bubble" }, /* Bubble effect */
                "onclick": { "enable": true, "mode": "push" } /* Adds particles on click */
            },
            "modes": {
                "bubble": { "distance": 150, "size": 6, "duration": 2, "opacity": 1, "speed": 3 },
                "push": { "particles_nb": 10 } /* Increased particles on click */
            }
        },
        "retina_detect": true
    });

    /* Custom Glow Effect */
    const canvas = document.querySelector("#particles-js canvas");
    if (canvas) {
        canvas.style.filter = "drop-shadow(0px 0px 6px #17a2b8)";
    }
</script>
<script>
    document.addEventListener("DOMContentLoaded", function () {
        const tabs = document.querySelectorAll(".exp-tab");
        const details = document.querySelectorAll(".exp-detail");
    
        tabs.forEach(tab => {
            tab.addEventListener("click", function () {
                // Remove active class from all tabs
                tabs.forEach(t => t.classList.remove("active"));
                this.classList.add("active");
    
                // Hide all experience details
                details.forEach(detail => detail.classList.remove("active"));
    
                // Show the clicked tab's content
                const target = this.getAttribute("data-target");
                document.getElementById(target).classList.add("active");
            });
        });
    });
    </script>
    

</body>
</html>