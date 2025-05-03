 <!DOCTYPE html>
	<html lang="en">
	<head>
	    <meta charset="UTF-8">
	    <meta name="viewport" content="width=device-width, initial-scale=1.0">
	    <title>Emmanuella Kupa | Business & Accounting Professional</title>
	    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
	    <style>
	        :root {
	            --primary: #7B2CBF;
	            --secondary: #9D4EDD;
	            --accent: #FF9E00;
	            --dark: #240046;
	            --light: #F8F9FA;
	        }
	

	        * {
	            margin: 0;
	            padding: 0;
	            box-sizing: border-box;
	        }
	

	        body {
	            font-family: 'Poppins', sans-serif;
	            background: linear-gradient(135deg, var(--dark), var(--primary));
	            color: var(--light);
	            overflow-x: hidden;
	            line-height: 1.7;
	        }
	

	        @keyframes float {
	            0%, 100% { transform: translateY(0); }
	            50% { transform: translateY(-20px); }
	        }
	

	        @keyframes fadeIn {
	            from { opacity: 0; transform: translateY(20px); }
	            to { opacity: 1; transform: translateY(0); }
	        }
	

	        @keyframes pulse {
	            0%, 100% { transform: scale(1); }
	            50% { transform: scale(1.05); }
	        }
	

	        /* Header with animated gradient */
	        header {
	            height: 100vh;
	            display: flex;
	            flex-direction: column;
	            justify-content: center;
	            align-items: center;
	            text-align: center;
	            padding: 0 20px;
	            position: relative;
	            overflow: hidden;
	        }
	

	        header::before {
	            content: '';
	            position: absolute;
	            top: 0;
	            left: 0;
	            width: 100%;
	            height: 100%;
	            background: linear-gradient(45deg, var(--primary), var(--secondary), var(--accent), var(--primary));
	            background-size: 400% 400%;
	            animation: gradientBG 15s ease infinite;
	            z-index: -1;
	            opacity: 0.7;
	        }
	

	        @keyframes gradientBG {
	            0% { background-position: 0% 50%; }
	            50% { background-position: 100% 50%; }
	            100% { background-position: 0% 50%; }
	        }
	

	        header h1 {
	            font-size: 4rem;
	            margin-bottom: 1rem;
	            font-weight: 700;
	            text-shadow: 0 5px 15px rgba(0,0,0,0.3);
	            animation: fadeIn 1s ease-out;
	        }
	

	        .header-contact {
	            margin-bottom: 2rem;
	            font-size: 1.2rem;
	            animation: fadeIn 1.5s ease-out;
	        }
	

	        .header-contact a {
	            color: white;
	            margin: 0 10px;
	            text-decoration: none;
	            transition: all 0.3s ease;
	        }
	

	        .header-contact a:hover {
	            color: var(--accent);
	        }
	

	        .typing-text {
	            font-size: 1.8rem;
	            margin-bottom: 2rem;
	            min-height: 2.5rem;
	            color: rgba(255,255,255,0.9);
	        }
	

	        .scroll-down {
	            position: absolute;
	            bottom: 30px;
	            left: 50%;
	            transform: translateX(-50%);
	            color: white;
	            font-size: 2rem;
	            animation: bounce 2s infinite;
	            cursor: pointer;
	        }
	

	        @keyframes bounce {
	            0%, 20%, 50%, 80%, 100% { transform: translateY(0) translateX(-50%); }
	            40% { transform: translateY(-20px) translateX(-50%); }
	            60% { transform: translateY(-10px) translateX(-50%); }
	        }
	

	        /* Navigation */
	        nav {
	            position: fixed;
	            top: 0;
	            left: 0;
	            width: 100%;
	            padding: 20px 0;
	            z-index: 100;
	            transition: all 0.3s ease;
	            backdrop-filter: blur(10px);
	            background-color: rgba(36, 0, 70, 0.7);
	        }
	

	        nav.scrolled {
	            padding: 10px 0;
	            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
	        }
	

	        .nav-container {
	            display: flex;
	            justify-content: space-between;
	            align-items: center;
	            max-width: 1200px;
	            margin: 0 auto;
	            padding: 0 20px;
	        }
	

	        .logo {
	            font-size: 1.8rem;
	            font-weight: 700;
	            color: white;
	            text-decoration: none;
	        }
	

	        .nav-links {
	            display: flex;
	            gap: 30px;
	        }
	

	        .nav-links a {
	            color: white;
	            text-decoration: none;
	            font-weight: 500;
	            position: relative;
	            transition: all 0.3s ease;
	            padding: 5px 0;
	        }
	

	        .nav-links a::after {
	            content: '';
	            position: absolute;
	            bottom: 0;
	            left: 0;
	            width: 0;
	            height: 2px;
	            background-color: var(--accent);
	            transition: width 0.3s ease;
	        }
	

	        .nav-links a:hover::after {
	            width: 100%;
	        }
	

	        .nav-links a:hover {
	            color: var(--accent);
	        }
	

	        .menu-toggle {
	            display: none;
	            cursor: pointer;
	            font-size: 1.5rem;
	        }
	

	        /* Sections */
	        section {
	            padding: 100px 20px;
	            max-width: 1200px;
	            margin: 0 auto;
	            opacity: 0;
	            transform: translateY(50px);
	            transition: all 0.8s ease;
	        }
	

	        section.visible {
	            opacity: 1;
	            transform: translateY(0);
	        }
	

	        h2 {
	            font-size: 2.5rem;
	            margin-bottom: 50px;
	            text-align: center;
	            position: relative;
	            display: inline-block;
	            left: 50%;
	            transform: translateX(-50%);
	        }
	

	        h2::after {
	            content: '';
	            position: absolute;
	            bottom: -10px;
	            left: 50%;
	            transform: translateX(-50%);
	            width: 80px;
	            height: 4px;
	            background-color: var(--accent);
	            border-radius: 2px;
	        }
	

	        /* About Section */
	        #about {
	            background-color: rgba(255,255,255,0.05);
	            border-radius: 20px;
	            margin: 50px auto;
	            padding: 50px;
	            backdrop-filter: blur(10px);
	            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
	        }
	

	        #about p {
	            font-size: 1.1rem;
	            line-height: 1.8;
	            margin-bottom: 20px;
	        }
	

	        .highlight {
	            color: var(--accent);
	            font-weight: 600;
	        }
	

	        /* Cards */
	        .cards-container {
	            display: grid;
	            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
	            gap: 30px;
	            margin-top: 50px;
	        }
	

	        .card {
	            background: rgba(255,255,255,0.05);
	            border-radius: 15px;
	            padding: 30px;
	            transition: all 0.5s ease;
	            backdrop-filter: blur(10px);
	            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
	            border: 1px solid rgba(255,255,255,0.1);
	        }
	

	        .card:hover {
	            transform: translateY(-10px);
	            box-shadow: 0 15px 30px rgba(0,0,0,0.3);
	            background: rgba(255,255,255,0.1);
	        }
	

	        .card h3 {
	            font-size: 1.5rem;
	            margin-bottom: 15px;
	            color: var(--accent);
	            display: flex;
	            align-items: center;
	        }
	

	        .card h3 i {
	            margin-right: 10px;
	        }
	

	        .card .date {
	            display: inline-block;
	            background-color: var(--dark);
	            padding: 5px 10px;
	            border-radius: 20px;
	            font-size: 0.8rem;
	            margin-bottom: 15px;
	        }
	

	        .card .location {
	            font-style: italic;
	            margin-bottom: 15px;
	            color: #dcdcdc;
	        }
	

	        .card ul {
	            list-style-position: inside;
	            padding-left: 5px;
	        }
	

	        .card li {
	            margin-bottom: 10px;
	            position: relative;
	            padding-left: 20px;
	        }
	

	        .card li::before {
	            content: '▹';
	            position: absolute;
	            left: 0;
	            color: var(--accent);
	        }
	

	        /* Skills */
	        .skills-container {
	            display: grid;
	            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
	            gap: 20px;
	            margin-top: 50px;
	        }
	

	        .skill {
	            background: rgba(255,255,255,0.05);
	            border-radius: 10px;
	            padding: 20px;
	            text-align: center;
	            transition: all 0.3s ease;
	            position: relative;
	            overflow: hidden;
	            border: 1px solid rgba(255,255,255,0.1);
	        }
	

	        .skill:hover {
	            transform: translateY(-5px);
	            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
	        }
	

	        .skill::before {
	            content: '';
	            position: absolute;
	            top: 0;
	            left: 0;
	            width: 100%;
	            height: 5px;
	            background: linear-gradient(90deg, var(--accent), var(--secondary));
	        }
	

	        .skill i {
	            font-size: 2.5rem;
	            margin-bottom: 15px;
	            color: var(--accent);
	        }
	

	        .skill h4 {
	            font-size: 1.2rem;
	            margin-bottom: 10px;
	        }
	

	        /* Projects */
	        .project-card {
	            background: rgba(255,255,255,0.05);
	            border-radius: 15px;
	            padding: 25px;
	            margin-bottom: 30px;
	            transition: all 0.3s ease;
	            backdrop-filter: blur(10px);
	        }
	

	        .project-card:hover {
	            transform: translateY(-5px);
	            box-shadow: 0 10px 25px rgba(0,0,0,0.2);
	        }
	

	        .project-card h3 {
	            color: var(--accent);
	            margin-bottom: 15px;
	            font-size: 1.4rem;
	        }
	

	        /* Contact */
	        #contact {
	            text-align: center;
	        }
	

	        .contact-links {
	            display: flex;
	            justify-content: center;
	            gap: 30px;
	            margin-top: 50px;
	            flex-wrap: wrap;
	        }
	

	        .contact-link {
	            display: flex;
	            align-items: center;
	            color: white;
	            text-decoration: none;
	            font-size: 1.2rem;
	            padding: 15px 30px;
	            border-radius: 50px;
	            transition: all 0.3s ease;
	            background: rgba(255,255,255,0.05);
	            border: 1px solid rgba(255,255,255,0.1);
	        }
	

	        .contact-link:hover {
	            background: var(--accent);
	            color: var(--dark);
	            transform: translateY(-5px);
	            box-shadow: 0 10px 20px rgba(255,158,0,0.3);
	        }
	

	        .contact-link i {
	            margin-right: 10px;
	            font-size: 1.5rem;
	        }
	

	        /* Footer */
	        footer {
	            text-align: center;
	            padding: 50px 20px;
	            background-color: rgba(0,0,0,0.2);
	            margin-top: 100px;
	        }
	

	        .social-links {
	            display: flex;
	            justify-content: center;
	            gap: 20px;
	            margin: 30px 0;
	        }
	

	        .social-link {
	            width: 50px;
	            height: 50px;
	            border-radius: 50%;
	            display: flex;
	            align-items: center;
	            justify-content: center;
	            background: rgba(255,255,255,0.1);
	            color: white;
	            font-size: 1.5rem;
	            transition: all 0.3s ease;
	        }
	

	        .social-link:hover {
	            background: var(--accent);
	            color: var(--dark);
	            transform: translateY(-5px);
	        }
	

	        .copyright {
	            margin-top: 20px;
	            font-size: 0.9rem;
	            color: rgba(255,255,255,0.7);
	        }
	

	        /* Floating elements */
	        .floating {
	            position: absolute;
	            animation: float 6s ease-in-out infinite;
	            opacity: 0.7;
	            z-index: -1;
	        }
	

	        .shape-1 {
	            top: 20%;
	            left: 10%;
	            width: 100px;
	            height: 100px;
	            background: radial-gradient(circle, var(--accent), transparent 70%);
	            border-radius: 50%;
	            filter: blur(20px);
	        }
	

	        .shape-2 {
	            top: 60%;
	            right: 15%;
	            width: 150px;
	            height: 150px;
	            background: radial-gradient(circle, var(--secondary), transparent 70%);
	            border-radius: 50%;
	            filter: blur(30px);
	            animation-delay: 2s;
	        }
	

	        .shape-3 {
	            bottom: 10%;
	            left: 20%;
	            width: 80px;
	            height: 80px;
	            background: radial-gradient(circle, var(--primary), transparent 70%);
	            border-radius: 50%;
	            filter: blur(15px);
	            animation-delay: 4s;
	        }
	

	        /* Responsive */
	        @media (max-width: 768px) {
	            header h1 {
	                font-size: 2.5rem;
	            }
	            
	            .header-contact {
	                font-size: 1rem;
	            }
	            
	            .typing-text {
	                font-size: 1.2rem;
	            }
	            
	            .nav-links {
	                position: fixed;
	                top: 80px;
	                left: 0;
	                width: 100%;
	                background-color: var(--dark);
	                flex-direction: column;
	                align-items: center;
	                padding: 20px 0;
	                gap: 15px;
	                transform: translateY(-150%);
	                transition: all 0.5s ease;
	            }
	            
	            .nav-links.active {
	                transform: translateY(0);
	            }
	            
	            .menu-toggle {
	                display: block;
	            }
	            
	            .cards-container {
	                grid-template-columns: 1fr;
	            }
	            
	            section {
	                padding: 70px 20px;
	            }
	            
	            .contact-links {
	                flex-direction: column;
	                gap: 15px;
	            }
	        }
	    </style>
	</head>
	<body>
	    <!-- Floating background elements -->
	    <div class="floating shape-1"></div>
	    <div class="floating shape-2"></div>
	    <div class="floating shape-3"></div>
	

	    <!-- Navigation -->
	    <nav id="navbar">
	        <div class="nav-container">
	            <a href="#" class="logo">EK</a>
	            <div class="menu-toggle">
	                <i class="fas fa-bars"></i>
	            </div>
	            <div class="nav-links">
	                <a href="#about">About</a>
	                <a href="#education">Education</a>
	                <a href="#experience">Experience</a>
	                <a href="#projects">Projects</a>
	                <a href="#skills">Skills</a>
	                <a href="#contact">Contact</a>
	            </div>
	        </div>
	    </nav>
	

	    <!-- Header -->
	    <header>
	        <h1>Emmanuella Kupa</h1>
	        <div class="header-contact">
	            <a href="mailto:Kupaemmanuella@gmail.com"><i class="fas fa-envelope"></i> Kupaemmanuella@gmail.com</a>
	            <a href="https://www.linkedin.com/in/emmanuella-kupa-92590822b/" target="_blank"><i class="fab fa-linkedin"></i> LinkedIn</a>
	        </div>
	        <div class="typing-text"></div>
	        <a href="#about" class="scroll-down">
	            <i class="fas fa-chevron-down"></i>
	        </a>
	    </header>
	

	    <!-- About Section -->
	    <section id="about">
	        <h2>Professional Summary</h2>
	        <div class="card">
	            <p>
	                Enthusiastic bilingual in French and English, who strives for excellence and growth in each educational and work opportunity earned. Currently a 3rd year student pursuing an <span class="highlight">Advanced Diploma in Business Administration and Accounting (Co-op) </span> from Niagara College.
	            </p>
	            <p>
	                Recognized for excellent interpersonal skills, professional behavior, and the ability to thrive in a collaborative, cross-cultural environment that prioritizes mutual respect and support among collaborators.
	            </p>
	            <p>
	                Actively seeking <span class="highlight">Summer 2025 Co-op opportunities</span> to apply my classroom knowledge in a professional setting while continuing to develop expertise in accounting and business administration.
	            </p>
	        </div>
	    </section>
	

	    <!-- Education Section -->
	    <section id="education">
	        <h2>Education</h2>
	        <div class="cards-container">
	            <div class="card">
	                <h3><i class="fas fa-graduation-cap"></i> Niagara College</h3>
	                <span class="date">2023 - 2026 (Expected)</span>
	                <p class="location">Niagara, ON</p>
	                <p><strong>Business Administration & Accounting (Co-op) Advanced Diploma</strong></p>
	                <ul>
	                    <li><strong>Relevant Coursework:</strong> Financial Accounting, Intermediate Accounting, Canadian Income Tax, Management Cost Accounting, Spreadsheet (Excel), Marketing, Organizational Behavior, Business Reports</li>
	                    <li><strong>Awards:</strong> English Academic Preparation scholarship for achieving an overall score of 95% and above (2022 & 2023) received ($3,500)</li>
	                    <li><strong>Technical Skills:</strong> Advanced proficiency in Microsoft Office Word, Excel, PowerPoint, Canva, Microsoft Team, and SharePoint</li>
	                    <li><strong>Certification:</strong> LinkedIn Certificate in Corporate Finance Foundations</li>
	                </ul>
	            </div>
	        </div>
	    </section>
	

	    <!-- Experience Section -->
	    <section id="experience">
	        <h2>Work Experience</h2>
	        <div class="cards-container">
	            <div class="card">
	                <h3><i class="fas fa-briefcase"></i> Coach - Tapestry</h3>
	                <span class="date">August 2024 - Present</span>
	                <p class="location">Niagara-on-the-Lake, ON</p>
	                <p><strong>Sales Associate III (Permanent Part-time)</strong></p>
	                <ul>
	                    <li>Delivered exceptional customer service, resulting in a 100% customer satisfaction rating by guiding consumers to suitable products using insights from fashion trends, discounts, and brand ambassador recommendations</li>
	                    <li>Streamlined inventory management procedures and implemented a new system that reduced monthly display reconstruction time by 15%</li>
	                </ul>
	            </div>
	

	            <div class="card">
	                <h3><i class="fas fa-headset"></i> CTC</h3>
	                <span class="date">May 2023 - September 2023</span>
	                <p class="location">Remote, ON</p>
	                <p><strong>Corporate Digital Customer Service Representative (Bilingual)</strong></p>
	                <ul>
	                    <li>Provided exceptional customer support to over 35 customers daily, addressing inquiries related to products, services, and technical issues across multiple communication channels (phone and email) while demonstrating bilingual skills in English and French</li>
	                    <li>Leveraged active listening skills to identify customer pain points, demonstrating empathy and providing personalized solutions by guiding customers step-by-step through resolving system errors, resulting in a 95% customer satisfaction rating</li>
	                </ul>
	            </div>
	

	            <div class="card">
	                <h3><i class="fas fa-mobile-alt"></i> Rawbank</h3>
	                <span class="date">November 2021 - April 2023</span>
	                <p class="location">Kinshasa, DRC</p>
	                <p><strong>Fintech Intern – Online & Commercial Banking Assistant</strong></p>
	                <ul>
	                    <li>Processed transactions efficiently, ensuring 100% accuracy in cashier services, contributing to seamless customer payment experiences</li>
	                    <li>Demonstrated problem-solving skills by resolving technical issues, optimizing the app's functionality, and guiding users through troubleshooting processes</li>
	                    <li>Leveraged effective communication to educate up to 75 clients on the app's benefits, increasing user adaptation by 50% and assisting them in conducting secure mobile transactions, reducing reliance on in-person banking by 15%</li>
	                </ul>
	            </div>
	        </div>
	    </section>
	

	    <!-- Projects Section -->
	    <section id="projects">
	        <h2>Key Projects</h2>
	        <div class="cards-container">
	            <div class="card">
	                <h3><i class="fas fa-chart-line"></i> Dashboard Project AT&T</h3>
	                <p><strong>Microsoft Excel Group Project</strong></p>
	                <ul>
	                    <li>Developed an Excel-based KPI dashboard for AT&T, utilizing pivot tables, map visualizations, and interactive dashboards to effectively analyze and present business performance metrics</li>
	                </ul>
	            </div>
	            <div class="card">
	                <h3><i class="fas fa-store"></i> Avondale Food Store Project</h3>
	                <p><strong>Business Report Project</strong></p>
	                <ul>
	                    <li>Developed a solution to improve the cash flow issues of Avondale Food Store by improving AR collection capability</li>
	                </ul>
	            </div>
	        </div>
	    </section>
	

	    <!-- Skills Section -->
	    <section id="skills">
	        <h2>Professional Skills</h2>
	        <div class="skills-container">
	            <div class="skill">
	                <i class="fas fa-file-invoice-dollar"></i>
	                <h4>Financial Accounting</h4>
	            </div>
	            <div class="skill">
	                <i class="fas fa-comments"></i>
	                <h4>Bilingual (English/French)</h4>
	            </div>
	            <div class="skill">
	                <i class="fas fa-users"></i>
	                <h4>Team Collaboration</h4>
	            </div>
	            <div class="skill">
	                <i class="fas fa-laptop"></i>
	                <h4>Microsoft Office Suite</h4>
	            </div>
	            <div class="skill">
	                <i class="fas fa-retweet"></i>
	                <h4>Process Improvement</h4>
	            </div>
	            <div class="skill">
	                <i class="fas fa-chart-pie"></i>
	                <h4>Data Analysis</h4>
	            </div>
	            <div class="skill">
	                <i class="fas fa-store"></i>
	                <h4>Retail Strategies</h4>
	            </div>
	            <div class="skill">
	                <i class="fas fa-mobile-alt"></i>
	                <h4>Fintech</h4>
	            </div>
	        </div>
	    </section>
	

	    <!-- Contact Section -->
	    <section id="contact">
	        <h2>Get In Touch</h2>
	        <p>I'm currently seeking co-op opportunities for Summer 2025 and would love to connect!</p>
	        
	        <div class="contact-links">
	            <a href="mailto:Kupaemmanuella@gmail.com" class="contact-link">
	                <i class="fas fa-envelope"></i> Email Me
	            </a>
	            <a href="https://www.linkedin.com/in/emmanuella-kupa-92590822b/" target="_blank" class="contact-link">
	                <i class="fab fa-linkedin"></i> LinkedIn
	            </a>
	        </div>
	    </section>
	

	    <!-- Footer -->
	    <footer>
	        <div class="social-links">
	            <a href="#" class="social-link"><i class="fab fa-linkedin"></i></a>
	            <a href="#" class="social-link"><i class="fab fa-github"></i></a>
	        </div>
	        <p class="copyright">© 2024 Emmanuella Kupa. All rights reserved.</p>
	    </footer>
	

	    <script>
	        // Typing animation
	        const texts = [
	            "Business Administration & Accounting Student",
	            "Bilingual Professional",
	            "Accounting Enthusiast learner",
	            "Co-op Seeker"
	        ];
	        let count = 0;
	        let index = 0;
	        let currentText = '';
	        let letter = '';
	        let isDeleting = false;
	        let typingSpeed = 100;
	

	        function type() {
	            currentText = texts[count];
	            
	            if (isDeleting) {
	                letter = currentText.slice(0, --index);
	                typingSpeed = 50;
	            } else {
	                letter = currentText.slice(0, ++index);
	                typingSpeed = 100;
	            }
	            
	            document.querySelector('.typing-text').textContent = letter;
	            
	            if (!isDeleting && letter.length === currentText.length) {
	                typingSpeed = 2000;
	                isDeleting = true;
	            } else if (isDeleting && letter.length === 0) {
	                isDeleting = false;
	                count = (count + 1) % texts.length;
	                typingSpeed = 500;
	            }
	            
	            setTimeout(type, typingSpeed);
	        }
	

	        // Start typing animation after 1 second
	        setTimeout(type, 1000);
	

	        // Scroll reveal animation
	        function checkScroll() {
	            const sections = document.querySelectorAll('section');
	            const windowHeight = window.innerHeight;
	            const scrollPosition = window.scrollY;
	            
	            sections.forEach(section => {
	                const sectionTop = section.offsetTop;
	                const sectionHeight = section.offsetHeight;
	                
	                if (scrollPosition + windowHeight > sectionTop + sectionHeight / 2) {
	                    section.classList.add('visible');
	                }
	            });
	        }
	

	        // Navbar scroll effect
	        function handleScroll() {
	            const navbar = document.getElementById('navbar');
	            if (window.scrollY > 100) {
	                navbar.classList.add('scrolled');
	            } else {
	                navbar.classList.remove('scrolled');
	            }
	            
	            checkScroll();
	        }
	

	        // Mobile menu toggle
	        document.querySelector('.menu-toggle').addEventListener('click', function() {
	            document.querySelector('.nav-links').classList.toggle('active');
	        });
	

	        // Smooth scrolling for anchor links
	        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
	            anchor.addEventListener('click', function(e) {
	                e.preventDefault();
	                document.querySelector(this.getAttribute('href')).scrollIntoView({
	                    behavior: 'smooth'
	                });
	                
	                // Close mobile menu if open
	                document.querySelector('.nav-links').classList.remove('active');
	            });
	        });
	

	        // Initialize scroll effects
	        window.addEventListener('scroll', handleScroll);
	        window.addEventListener('load', handleScroll);
	    </script>
	</body>
	</html>
