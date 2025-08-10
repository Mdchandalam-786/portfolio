<!DOCTYPE html>
<html lang="en">
<head>
    <style>
      :root {
    --primary: #2563eb;
    --dark: #1e293b;
    --light: #f8fafc;
    --gray: #94a3b8;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
/* Header & Navigation */
header {
    background-color:#e0e0e0;
    position: fixed;
    top: 0;
    width: 100%;
    padding: 1.5rem 5%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    backdrop-filter: blur(20px);
    z-index: 100;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

.logo {
    font-size: 1.8rem;
    font-weight: 700;
    color: var(--primary);
    text-decoration: none;
}

nav ul {
    display: flex;
    list-style: none;
    gap: 2rem;
}

nav a {
    color:black;
    text-decoration: none;
    font-weight: 500;
    transition: color 0.3s;
}

nav a:hover {
    color: var(--primary);
}

.menu-toggle {
    display: none;
    cursor: pointer;
    font-size: 1.5rem;
}

/* Hero Section */
.hero {
    height: 100vh;
    display: flex;
    align-items: center;
    padding: 0 5%;
    background: linear-gradient(135deg, #e0f2fe 0%, #f0fdfa 100%);
}

.hero-content {
    max-width: 600px;
}

.hero h1 {
    color: #1e293b;
    font-size: 3.5rem;
    margin-bottom: 1rem;
    line-height: 1.2;
}

.hero p {
    font-size: 1.2rem;
    color: var(--gray);
    margin-bottom: 2rem;
}

.btn {
    display: inline-block;
    padding: 0.8rem 1.8rem;
    backdrop-filter:blur(5px);
    filter:opacity(70%);
    background-color: var(--primary);
    color: white;
    border-color:blue;
    border-radius: 50px;
    text-decoration: none;
    font-weight: 500;
    transition: transform 0.3s, box-shadow 0.3s;
}

.btn:hover {
    filter: opacity(100%);
    transform: translateY(-3px);
    box-shadow: 0 10px 20px rgba(37, 99, 235, 0.2);
}

.hero-image {
    position: absolute;
    right: 5%;
    width: 40%;
    max-width: 600px;
    animation: float 6s ease-in-out infinite;
}

@keyframes float {
    0% { transform: translateY(0px); }
    50% { transform: translateY(-20px); }
    100% { transform: translateY(0px); }
}

/* Sections */
section {
    padding: 6rem 5%;
}

.section-title {
    text-align: center;
    margin-bottom: 4rem;
}

.section-title h2 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
}

.section-title p {
    color: var(--gray);
    max-width: 600px;
    margin: 0 auto;
}

/* Projects */
.projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 2rem;
}

.project-card {
    backdrop-filter:blur(10px);
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s;
}

.project-card:hover {
    cursor: pointer;
    transform: translateY(-20px);
}
.project-card:focus{
    border: 1px solid white;
}

.project-image {
    height: 200px;
    overflow: hidden;
}

.project-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.5s;
}

.project-card:hover .project-image img {
    transform: scale(1.1);
}

.project-info {
    padding: 1.5rem;
}

.project-info h3 {
    margin-bottom: 0.5rem;
    color: white;
}

.project-info p {
    color:white;
    margin-bottom: 1rem;
}

.project-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-bottom: 1rem;
}

.tag {
    background-color: #dbeafe;
    color: var(--primary);
    padding: 0.3rem 0.8rem;
    border-radius: 50px;
    font-size: 0.8rem;
    font-weight: 500;
}

/* Skills */
.skills-container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 2rem;
}

.skill-card {
    backdrop-filter:blur(2px);
    padding: 2rem;
    border-radius: 10px;
    text-align: center;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s;
}

.skill-card:hover {
    transform: translateY(-10px);
    backdrop-filter:blur(5px);
    border:2px solid white;
}

.skill-icon {
    font-size: 3rem;
    color:white;
    margin-bottom: 1rem;
}
section h3{
    color: white;
}
section h2{
    color:white;
}
section p{
    color: white;
}

/* About */
#about{
    background-color:#02183f ;
    background-size:100% 100%;
}
.about-content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: center;
}

.about-image {
    background-image: url('e.jpg');
    border-radius:38% 62% 37% 63% / 31% 73% 27% 69% ;
    overflow: hidden;
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
    filter:opacity(70%);
    background-size:100% 100%;
    box-shadow: -12px 12px 15px 2px rgba(0,0,0,0.2);
    animation: float 6s ease-in-out infinite;
}
.img{
    overflow: hidden;
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
    background-size:100% 100%;
}
.img img{
    width: 100% ;
    height: auto;
    display: block;
}

.about-image img {
    width: 100% ;
    height: auto;
    display: block;
}

.about-text p {
    margin-bottom: 1.5rem;
}

/* Contact */
#contact{
    background-color:#02183f;
    background-size:100% 100%;
}
.contact-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
}

.contact-info {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
}

.contact-item {
    display: flex;
    align-items: center;
    gap: 1rem;
}
.contact-section {
    background: rgba(255, 255, 255, 0.1);
    padding: 2rem;
    border-radius: 10px;
}
.contact-icon {
    backdrop-filter:blur(2px);
    width: 50px;
    height: 50px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--primary);
    font-size: 1.2rem;
    border:1px solid black;
    transition: 0.3s;
}
.contact-icon:hover{
    transform:translatey(-5px);
    border:1px solid white;
}
.contact-form {
    backdrop-filter:blur(5px);
    padding: 2rem;
    border-radius: 10px;
    box-shadow: 5px 5px 15px rgba(114, 113, 113, 0.1);
}

.form-group {
    margin-bottom: 1.5rem;
}

.form-group label {
    color: white;
    display: block;
    margin-bottom: 0.5rem;
    font-weight: 500;
}

.form-group input,
.form-group textarea {
    width: 100%;
    padding: 0.8rem;
    border: 1px solid #e2e8f0;
    border-radius: 5px;
    font-size: 1rem;
}

.form-group textarea {
    min-height: 150px;
    resize: vertical;
}
/* Footer */
footer {
    background-color:rgb(20, 19, 19);
    color: white;
    padding: 3rem 5%;
    text-align: center;
}

.social-links {
color: #dbeafe;
    display: flex;
    justify-content: center;
    gap: 1.5rem;
    margin: 2rem 0;
}

.social-links a {
    font-size: 1.5rem;
    transition: color 0.3s;
}

.social-links a:hover {
    color: var(--primary);
}

.copyright {
    color: var(--gray);
    font-size: 0.9rem;
}

/* Responsive */
@media (max-width: 992px) {
    .hero-image {
        width: 100%;
        height: 300px;
        margin-top: 2rem;
    }
    
    .hero-content {
        max-width: 100%;
        text-align: center;
    }
    
    .about-content,
    .contact-container {
        grid-template-columns: 1fr;
    }
    
    .about-image {
        order: -1;
        display: none;
    }
    #contact img{
        height:auto;
        width:auto;
    }
    #contact .img{
        margin-bottom:20vh;
        height:10vh;
        width:10vh;
        border-radius:50%;
        filter:drop-shadow(10px 10px 2px black);

    }

    .pr{
        background-color: #000000;
    }
}

@media (max-width: 768px) {
    nav ul {
        position: fixed;
        top: 80px;
        left: -100%;
        width: 100%;
        height: calc(100vh - 80px);
        background-color: white;
        flex-direction: column;
        align-items: center;
        padding: 2rem 0;
        transition: left 0.3s;
    }
    
    nav ul.active {
        left: 0;
    }
    
    .menu-toggle {
        display: block;
    }
    
    .hero h1 {
        font-size: 2.5rem;
    }
}
    .hero{
        background-color:black;
        background-size:100% 100%;
        box-shadow:20px 20px 10px black ;
    animation:slider 10s linear infinite;
}
@keyframes slider {
    0%{
            background-image:url("b.jpg");
    }
    25%{
            background-image:url("e.jpg");
    }
    50%{
            background-image:url("b.jpg");
    }
    75%{
            background-image:url("chand.jpg");
    }
    80%{
            background-image:url("e.jpg");
    }
    100%{
            background-image:url("chand.jpg");
    }
}
body{
    background-color: #02183f;

}
.hero-content{
    margin-top:30vh;
    margin-left:35vh;
}
.hero h1{
    color:white;
}
.hero a{
    margin-left:25vh;
}
.hero p{
    text-align: center;

    color:rgb(250, 242, 242);
}
header ul a{
    color: white;
}
header{
    background-color:transparent;
    
}
header a h1{
    color: white;
}
header a h1:hover{
    color: #2563eb;
}
#projects{
        background-color: #02183f;
        background-size:100% 100%;
        box-shadow:20px 20px 10px rgb(197, 197, 197) ;
}
#skills{
    background-color:#02183f;
    background-size:100% 100%;
}
section form input {
    background-color:transparent;
}
section form textarea{
    border:none;
    background-color:transparent;
} 
section form{
    border:1px solid white ;
}
section form .btn{
    cursor:pointer;
}
#skills h2{
    
    background-image: url('3.jpg');
    color: transparent;
    -webkit-background-clip: text;
    background-clip: text;
}
            /* Portfolio Background */
body {
    min-height: 100vh;
    background: linear-gradient(120deg, #e0e7ff 0%, #f0fdfa 100%);
    position: relative;
    font-family: 'Segoe UI', Arial, sans-serif;
    overflow-x: hidden;
}

/* Decorative circles for modern effect */
body::before, body::after {
    content: '';
    position: absolute;
    border-radius: 50%;
    z-index: 0;
    opacity: 0.18;
}
.hero h1{
    animation: bounce-top 0.9s both;
}
@keyframes bounce-top{
    0%{
        transform: translateY(-160px);
        animation-timing-function:ease-in;
        opacity: 1;

    }
    24%{
        opacity: 1;
    }
    40%{
        transform: translateY(-48px);
        animation-timing-function:ease-in;
    }
    65%{
        transform:translateY(-24px);
        animation-timing-function:ease-in;
    }
    82%{
        transform:translateY(-12px);
        animation-timing-function:ease-in;
    }
    93%{
        transform:translateY(-8px);
        animation-timing-function:ease-in;
    }
    25%,
    55%,
    75%,
    87%{
        transform: translateY(0px);
        animation-timing-function:ease-out;
    }
    100%{
        transform:translateY(0px);
        animation-timing-function:ease-out;
        opacity:1;
    }
}     
    </style>
    <title>chand</title>
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <link rel="stylesheet" href="chand.css">
    <style>
        
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <a href="#" class="logo"><h1>C<span>A</span></h1></a>
        <nav>
            <div class="menu-toggle">
                <i class="fas fa-bars"></i>
            </div>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>

    </header>   

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
    <h1>Hi, I'm Md chand alam</h1>
    <p>A passionate web designer creating beautiful, 
        functional websites that deliver results.</p>
            <a href="#projects" class="btn">View My Work</a>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <div class="section-title">
            <h2 style="color:white;">My Projects</h2>
        </div>
        <div class="projects-grid">
            <div class="project-card">
                <div class="project-image">
                    <img src="e.jpg">
                </div>
                <div class="project-info">
                    <h3 style="text-align: center;">E-commerce Website</h3>
                    <p style="text-align: center;">A fully responsive online store with product filtering and cart functionality.</p>
                    <div class="project-tags" style="display:flex; justify-content: center;">
                        <span class="tag">HTML</span>
                        <span class="tag">CSS</span>
                        <span class="tag">JavaScript</span>
                        <span class="tag">React</span>
                    </div>
                    <a href="#" class="btn">View Project</a>
                </div>
            </div>
            
            <div class="project-card">
                <div class="project-image">
                    <img src="https://images.unsplash.com/photo-1559028012-481c04fa702d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80" alt="Portfolio Website">
                </div>
                <div class="project-info">
                    <h3 style="text-align: center;">Artist Portfolio</h3>
                    <p style="text-align: center;">A minimalist portfolio website showcasing an artist's work with smooth animations.</p>
                    <div class="project-tags" style="display: flex; justify-content: center;">
                        <span class="tag">HTML</span>
                        <span class="tag">CSS</span>
                        <span class="tag">JavaScript</span>
                        <span class="tag">GSAP</span>
                    </div>
                    <a href="#" class="btn" >View Project</a>
                </div>
            </div>
            
            <div class="project-card">
                <div class="project-image">
                <img src="b.jpg" alt="">

                </div>
                <div class="project-info">
                    <h3 style="text-align: center;">Corporate Website</h3>
                    <p style="text-align: center;">A professional website for a financial services company with CMS integration.</p>
                    <div class="project-tags" style="display:flex; justify-content:center;">
                        <span class="tag">WordPress</span>
                        <span class="tag">PHP</span>
                        <span class="tag">JavaScript</span>
                    </div>
                    <a href="#" class="btn">View Project</a>
                </div>
            </div>
                
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills">
        <div class="section-title">
            <h2>My Skills</h2>
        </div>
        <div class="skills-container">
            <div class="skill-card">
                <div class="skill-icon">
                    <i class="fab fa-html5"></i>
                </div>
                <h3>HTML5</h3>
                <p>Semantic markup for accessible, SEO-friendly websites.</p>
            </div>
            
            <div class="skill-card">
                <div class="skill-icon">
                    <i class="fab fa-css3-alt"></i>
                </div>
                <h3>CSS</h3>
                <p>Modern styling with animations, transitions and responsive design.</p>
            </div>
            
            <div class="skill-card">
                <div class="skill-icon">
                    <i class="fab fa-js"></i>
                </div>
                <h3>JavaScript</h3>
                <p>Interactive elements and dynamic content for engaging experiences.</p>
            </div>
            
            <div class="skill-card">
                <div class="skill-icon">
                    <i class="fab fa-react"></i>
                </div>
                <h3>Bootstrap</h3>
                <p>Building component-based applications with modern JavaScript.</p>
            </div>
            
            <div class="skill-card">
                <div class="skill-icon">
                    <i class="fas fa-mobile-alt"></i>
                </div>
                <h3>Responsive Design</h3>
                <p>Websites that look great on any device.</p>
            </div>
            
            <div class="skill-card">
                <div class="skill-icon">
                    <i class="fas fa-paint-brush"></i>
                </div>
                <h3>UI/UX Design</h3>
                <p>Creating intuitive, user-friendly interfaces.</p>
            </div>
            <div class="skill-card">
                <div class="skill-icon">
                    <i class="fas fa-code"></i>
                </div>
                <h3>Version Control</h3>
                <p>Using Git for collaborative development and code management.</p>
            </div>
            <div class="skill-card">
                <div class="skill-icon">
                    <i class="fas fa-server"></i>
                </div>
                <h3>Backend Development</h3>
                <p>Building robust server-side applications with Node.js and Express.</p>
                </div>
                 <div class="skill-card">
                <div class="skill-icon">
                    <i class="fas fa-server"></i>
                </div>
                <h3>Backend Development</h3>
                <p>Building robust server-side applications with Node.js and Express.</p>
                </div>
                 <div class="skill-card">
                <div class="skill-icon">
                <i class="fas fa-code"></i>
                </div>
                <h3>Full Stack Development</h3>
                <p>End-to-end web solutions, from front-end interfaces to back-end servers and databases.</p>
                </div>
                
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <div class="section-title">
            <h2>About Me</h2>
            <p style="color: white;">Learn more about who I am and what drives my passion for web design.</p>
        </div>
        <div class="about-content">
            <div class="about-text">
                <p>I'm a web designer with over 1 years of experience creating digital experiences that are both beautiful and functional. My journey began when I built my first website at 5, and I've been hooked ever since.</p>
                <p>What I love most about web design is the perfect blend of creativity and problem-solving. Every project is a new challenge to create something that not only looks great but also serves its purpose effectively.</p>
                <p>When I'm not designing, you can find me hiking in the mountains, reading sci-fi novels, or experimenting with new web technologies.</p>
                <a href="#contact" class="btn">Get In Touch</a>
            </div>
            <div class="about-image" >
                <img src="—Pngtree—business portfolio 3d character illustration_13355676.png" style="filter: drop-shadow(10px 10px 2px black);">
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <div class="section-title">
            <h2>Get In Touch</h2>
            <p style="color: white;">Have a project in mind or want to collaborate? I'd love to hear from you!</p>
        </div>
        <div class="contact-container">
            <div class="contact-info">
                <div class="contact-item">
                    <div class="contact-icon">
                        <i class="fas fa-envelope"></i>
                    </div>
                    <div>
                        <h3>Email</h3>
                        <p>Mdchand.redminote9@gmail.com</p>
                    </div>
                </div>
                
                <div class="contact-item">
                    <div class="contact-icon">
                        <i class="fas fa-phone"></i>
                    </div>
                    <div>
                        <h3>Phone</h3>
                        <p>+91 99117 06012</p>
                    </div>
                </div>
                
                <div class="contact-item">
                    <div class="contact-icon">
                        <i class="fas fa-map-marker-alt"></i>
                    </div>
                    <div>
                        <h3>Location</h3>
                    </div>
                </div>
            </div>
            
            <form class="contact-form">
                <div class="form-group">
                    <label for="name">Name</label>
                    <input type="text" id="name" required placeholder="enter your Name">
                </div>
                
                <div class="form-group">    
                    <label for="email">Email</label>
                    <input type="email" id="email" required placeholder="enter the Email">
                </div>
                
                <div class="form-group">
                    <label for="subject">Subject</label>
                    <input type="text" id="subject" required placeholder="enter your topic">
                </div>
                
                <div class="form-group">
                    <label for="message">Message</label>
                    <textarea id="message" required placeholder="enter the message"></textarea>
                </div>
                
                <button type="submit" class="btn">Send Message</button>
            </form>
        </div>
        <div>
    </section>

    <!-- Footer -->
    <footer>
        <h2>Md chand alam</h2>
        <p>Web Designer & Developer</p>
        <div class="social-links">
            <a href="#"><i class="fab fa-dribbble"></i></a>
            <a href="#"><i class="fab fa-behance"></i></a>
            <a href=""><i class="fab fa-github"></i></a>
            <a href="#"><i class="fab fa-linkedin-in"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
        </div>
        <p class="copyright">© 2025 Md chand alam. All rights reserved.</p>
    </footer>

    <script src="chand.js"> </script>
    <script>
       // Mobile menu toggle
   const menuToggle = document.querySelector('.menu-toggle');
   const nav = document.querySelector('nav ul');
   
   menuToggle.addEventListener('click', () => {
       nav.classList.toggle('active');
   });
   
   // Smooth scrolling for navigation links
   document.querySelectorAll('nav a').forEach(anchor => {
       anchor.addEventListener('click', function(e) {
           e.preventDefault();
           
           const targetId = this.getAttribute('href');
           const targetElement = document.querySelector(targetId);
           
           window.scrollTo({
               top: targetElement.offsetTop - 80,
               behavior: 'smooth'
           });
           
           // Close mobile menu if open
           nav.classList.remove('active');
       });
   });
   
   // Form submission
   const contactForm = document.querySelector('.contact-form');
   contactForm.addEventListener('submit', function(e) {
       e.preventDefault();
       alert('Thank you for your message! I will get back to you soon.');
       this.reset();
   });
    </script>
      
    </script>
</body>
</html>
