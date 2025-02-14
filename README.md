<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Nulu Ritika - Front-end Developer Portfolio">
    <title>Nulu Ritika | Portfolio</title>
    <link rel="icon" href="assets/logo.png" type="image/png">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/4.6.0/css/bootstrap.min.css">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            overflow-x: hidden;
            scroll-behavior: smooth;
            color: #2c3e50;
        }

        h1,
        h2,
        h3,
        h4,
        h5,
        h6 {
            font-family: 'Montserrat', sans-serif;
            font-weight: 600;
        }

        /* ======================= Navbar ========================= */
        nav {
            background: #000;
            transition: background 0.5s;
        }

        nav a {
            color: white;
            transition: 0.3s;
        }

        nav a:hover {
            color: #c29752;
        }

        .navbar-brand {
            font-weight: bold;
            font-size: 1.8rem;
            color: #c29752;
        }

        /* ======================= Animations Keyframes ========================= */
        @keyframes fadeIn {
            0% {
                opacity: 0;
                transform: translateY(30px);
            }

            100% {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes zoomIn {
            0% {
                opacity: 0;
                transform: scale(0.9);
            }

            100% {
                opacity: 1;
                transform: scale(1);
            }
        }

        @keyframes slideUp {
            0% {
                opacity: 0;
                transform: translateY(100px);
            }

            100% {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes bounce {

            0%,
            20%,
            50%,
            80%,
            100% {
                transform: translateY(0);
            }

            40% {
                transform: translateY(-10px);
            }

            60% {
                transform: translateY(-5px);
            }
        }

        /* ======================= Hero Section ========================= */
        .hero {
            background: linear-gradient(135deg, #1a1a1a, #2c3e50);
            color: white;
            padding: 160px 20px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero h1 span {
            background: linear-gradient(to right, #e4de32, #ffcc00);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;

        }

        .hero .btn {
            margin: 10px;
            padding: 12px 30px;
            font-size: 1.1rem;
            transition: transform 0.3s;
        }

        .hero .btn:hover {
            transform: translateY(-5px);
        }

        .btn-primary {
            background-color: #c29752;
            border: none;
        }

        .btn-outline-light {
            border: 2px solid white;
            color: white;
        }

        /* ======================= About Section ========================= */
        #about {
            padding: 100px 20px;
            background: #f9f9f9;
            opacity: 0;
            transition: all 0.8s ease-in-out;
        }

        #about.show {
            opacity: 1;
            transform: translateY(0);
        }

        #about h2 {
            color: #333;
            font-weight: bold;
        }

        /* ======================= Projects Section ========================= */
        #projects {
            padding: 100px 20px;
            background-color: #fff;
            opacity: 0;
            transition: all 0.8s ease-in-out;
        }

        #projects.show {
            opacity: 1;
            transform: translateY(0);
        }

        .project-card {
            border: 1px solid #ddd;
            padding: 20px;
            margin-bottom: 30px;
            transition: transform 0.3s ease-in-out;
            animation: zoomIn 0.8s ease-out;
        }

        .project-card img {
            width: 100%;
            border-radius: 5px;
        }

        .project-card h4 {
            margin: 15px 0 10px;
            font-weight: bold;
        }

        .project-card:hover {
            transform: translateY(-8px) scale(1.03);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }

        .project-card {
            background: #fff;
            padding: 15px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
            min-height: 350px;
            /* Ensuring equal height */
        }

        .project-card img {
            max-width: 100%;
            border-radius: 5px;
        }

        .project-card h4 {
            font-size: 18px;
            font-weight: 600;
            margin-top: 10px;
        }

        .project-card p {
            font-size: 14px;
            color: #555;
        }

        .project-card:hover {
            transform: translateY(-5px);
        }


        /* ======================= Skills Section ========================= */
        #skills {
            padding: 10% 5%;
            background: #f0f0f0;
            opacity: 0;
            transition: all 0.8s ease-in-out;
        }

        #skills.show {
            opacity: 1;
            transform: translateY(0);
        }

        .skill-item {
            text-align: center;
            margin-bottom: 30px;
            animation: bounce 1.5s infinite;
        }

        .skill-item i {
            border: 2px solid grey;
            padding: 3%;
            border-radius: 5px;
            font-size: 3rem;
            color: #c29752;
        }

        .skill-item h5 {
            margin-top: 15px;
        }

        .skillsection {
            align-items: center;
            text-align: center;

        }


        /* ======================= Contact Section ========================= */
        #contact {
            padding: 100px 20px;
            background: #111;
            color: white;
            opacity: 0;
            transition: all 0.8s ease-in-out;
        }

        #contact.show {
            opacity: 1;
            transform: translateY(0);
        }

        .contact-form .form-control {
            margin-bottom: 15px;
            transition: box-shadow 0.3s ease-in-out;
        }

        .contact-form .form-control:focus {
            box-shadow: 0 0 8px rgba(194, 151, 82, 0.7);
        }

        /* ======================= Footer ========================= */
        footer {
            background-color: #000;
            color: #aaa;
            padding: 20px 0;
            font-size: 0.9rem;
        }

        footer a {
            color: #c29752;
            text-decoration: none;
        }

        footer a:hover {
            text-decoration: underline;
        }

        /* ======================= Scroll to Top Button ========================= */
        .scroll-top {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: #c29752;
            color: white;
            border-radius: 50%;
            padding: 12px 16px;
            cursor: pointer;
            transition: background 0.3s, transform 0.3s;
            display: none;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
        }

        .scroll-top:hover {
            background-color: #8c6c3f;
            transform: translateY(-5px);
        }

        #mywork {}
    </style>

</head>
<body>
    <!-- ======================== Navbar ========================= -->
    <nav class="navbar navbar-expand-lg navbar-dark fixed-top">
        <div class="container">
            <a class="navbar-brand" href="#">Nulu Ritika</a>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ml-auto">
                    <li class="nav-item"><a class="nav-link" href="#about">About</a></li>
                    <li class="nav-item"><a class="nav-link" href="#projects">Projects</a></li>
                    <li class="nav-item"><a class="nav-link" href="#skills">Skills</a></li>
                    <li class="nav-item"><a class="nav-link" href="#contact">Contact</a></li>
                </ul>
            </div>
        </div>
    </nav>
    <!-- ======================== Hero Section ========================= -->
    <section class="hero">
        <div class="container">
            <h1>Hello, I'm <span>Nulu Ritika</span></h1>
            <p class="lead">A passionate Front-end Developer and CSE Undergraduate at C.V. Raman Global University</p>
            <a href="#projects" id="mywork" class="btn btn-primary">View My Work</a>
            <a href="" class="btn btn-outline-light" onclick="pdfdownload()">Download Resume</a>
        </div>
    </section>
    <!-- ======================== About Section ========================= -->
    <section id="about" class="text-center">
        <div class="container">
            <h2>About Me</h2>
            <p> I'm a Front-end Developer with a passion for building responsive and user-friendly web applications.
                Currently pursuing my Computer Science degree at C.V. Raman Global University, I love exploring new
                technologies and solving complex problems. </p>
        </div>
    </section>
    <!-- ======================== Projects Section ========================= -->
    <section id="projects">
        <div class="container">
            <h2 class="text-center mb-5">My Projects</h2>
            <div class="row">
                <div class="col-md-4">
                    <div class="project-card text-center">
                        <img src="images/rhyno2.jpg" alt="Project 1" class="img-fluid">
                        <h4 class="mt-3">Rhyno EV Electric Bike Website</h4>
                        <p>Designed using HTML, CSS, and JavaScript to showcase electric bike models with interactive
                            UI.</p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="project-card text-center">
                        <img src="images/food-ordering-logo.jpg" alt="Project 2" class="img-fluid">
                        <h4 class="mt-3">Food Ordering Website</h4>
                        <p>Developed a dynamic website with menu browsing, cart management, and order placement
                            features.</p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="project-card text-center">
                        <img src="images/wordpress2.jpg" alt="Project 3" class="img-fluid">
                        <h4 class="mt-3">Custom WordPress Theme</h4>
                        <p>Built a unique WordPress theme using HTML, CSS, JavaScript, and plugins for a modern design.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ======================== Skills Section ========================= -->
    <center>
        <section class="skillsection" id="skills">
            <div class="container text-center">
                <h2>Skills</h2>
                <div class="col-md-12">
                    <div class="row mt-5 justify-content-center gap-4">
                        <div class="col-md-3 skill-item" style=" border: 1px solid grey; padding: 2%; border-radius: 5px; margin-right: 15px;">
                            <i class="fab fa-html5"></i>
                            <h5>HTML5</h5>
                        </div>
                        <div class="col-md-3 skill-item" style=" margin-right: 15px; border: 1px solid grey; padding: 2%; border-radius: 5px;">
                            <i class="fab fa-css3-alt"></i>
                            <h5>CSS3</h5>
                        </div>
                        <div class="col-md-3 skill-item" style=" border: 1px solid grey; padding: 2%; border-radius: 5px;">
                            <i class="fab fa-js-square"></i>
                            <h5>JavaScript</h5>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </center>
    <!-- ======================== Contact Section ========================= -->
    <section id="contact">
        <div class="col-md-12 col-sm-12 col-xl-12">
            <div class="row">
                <div class="col-md-6">
                    <div class="container text-center">
                        <h2>Contact Me</h2>
                        <p>Feel free to reach out for collaborations or just a friendly hello!</p>
                        <form class="contact-form">
                            <input type="text" class="form-control" placeholder="Your Name" required>
                            <input type="email" class="form-control" placeholder="Your Email" required>
                            <textarea class="form-control" placeholder="Your Message" rows="5" required></textarea>
                            <button type="submit" class="btn btn-primary mt-3">Send Message</button>
                        </form>
                    </div>

                </div>
                <div class="col-md-6 text-center py-4" >
                   <div style="border: 2px solid white; border-radius: 5px; padding: 10%;">
                    <h3 class="mb-3">Visit Me</h3>
                    <p class="fst-italic">"A journey of a thousand lines of code begins with a single <strong>commit</strong>."</p>
                    <a href="https://aw-nuluritika.github.io/Rhyno/" target="_blank"
                        class="btn btn-light btn-sm fw-bold px-4 py-2 mt-2 shadow">
                        🚀 Check out my website
                    </a>
                   </div>
                </div>
                
            </div>
        </div>
    </section>
    <!-- ======================== Footer ========================= -->
    <footer class="text-center">
        <p>&copy; 2025 Nulu Ritika | Made with </p>
        <p>
            <a href="https://github.com/" target="_blank"><i class="fab fa-github"></i> GitHub</a> |
            <a href="https://linkedin.com/" target="_blank"><i class="fab fa-linkedin"></i> LinkedIn</a>
        </p>
    </footer>
    <!-- ======================== Scroll to Top Button ========================= -->
    <div class="scroll-top" onclick="scrollToTop()">
        <i class="fas fa-arrow-up"></i>
    </div>
    <!-- ======================== Scripts ========================= -->
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/4.6.0/js/bootstrap.bundle.min.js"></script>
    <script>
        // Scroll to Top
        window.addEventListener('scroll', () => {
            document.querySelector('.scroll-top').style.display = window.scrollY > 300 ? 'block' : 'none';
        });
        function scrollToTop() {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }
        // Scroll reveal animations
        const sections = document.querySelectorAll('section');
        window.addEventListener('scroll', () => {
            sections.forEach(section => {
                const sectionTop = section.getBoundingClientRect().top;
                if (sectionTop < window.innerHeight - 100) {
                    section.classList.add('show');
                }
            });
        });
    </script>
    <script>
        function pdfdownload() {
            var link = document.createElement('a');
            link.href = 'files/Nulu-Ritika-Web-Developer.pdf';
            link.download = 'Nulu-Ritika-Web-Developer.pdf';
            document.body.appendChild(link);
            link.click();
            document.body.removeChild(link);
        }
    </script>
</body>
</html>
