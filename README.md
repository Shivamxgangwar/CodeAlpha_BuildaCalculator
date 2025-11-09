# CodeAlpha_Portfolio
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Your Name | Portfolio</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>

  <!-- ===== Navigation ===== -->
  <header>
    <nav>
      <h1>Shivam Gangwar</h1>
      <ul class="nav-links">
        <li><a href="#about">About</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#resume">Resume</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <!-- ===== Hero Section (Your Picture) ===== -->
  <section id="hero">
    <div class="hero-content">
      <img src="images/shivam.jpeg" alt="" class="images/shivam.jpeg">
      <h2>Hello, I'm <span>Shivam Gangwar</span></h2>
      <p>A passionate Computer Science student skilled in C, C++, Java, Python, HTML, CSS, and JavaScript.</p>
      <a href="#contact" class="btn">Contact Me</a>
    </div>
  </section>

  <!-- ===== About Section ===== -->
  <section id="about">
    <h2>About Me</h2>
    <p>
      I'm a B.Sc. (Hons.) Computer Science student with a strong interest in software development, web design, and problem solving.
      I enjoy learning new technologies and applying my knowledge to build creative, user-friendly solutions.
    </p>
  </section>

  <!-- ===== Skills Section ===== -->
  <section id="skills">
    <h2>Technical Skills</h2>
    <div class="skills-container">
      <div class="skill-card">C</div>
      <div class="skill-card">C++</div>
      <div class="skill-card">Java</div>
      <div class="skill-card">Python</div>
      <div class="skill-card">HTML</div>
      <div class="skill-card">CSS</div>
      <div class="skill-card">JavaScript</div>
      
    </div>
  </section>

  <!-- ===== Projects Section ===== -->
  <section id="projects">
    <h2>Projects</h2>
    <div class="project-card">
      <img src="assets/images/project1.jpg" alt="Project Screenshot">
      <h3>My Portfolio Website</h3>
      <p>A responsive personal website built using HTML, CSS, and JavaScript.</p>
    </div>
    <div class="project-card">
      <img src="c:\Users\Dell\OneDrive\Desktop\Calculator\index.html\Screenshot 2025-11-09 082224.png" alt="Project Screenshot">
      <h3>Student Management System</h3>
      <p>Developed using C++ and file handling concepts to manage student data.</p>
    </div>
  </section>

  <!-- ===== Resume Section ===== -->
  <section id="resume">
    <h2>Resume</h2>
    <a href="assets/resume.pdf" target="_blank" class="btn">Download Resume</a>
  </section>

  <!-- ===== Contact Section ===== -->
  <section id="contact">
    <h2>Contact Me</h2>
    <p>Email: <a href="shivamxgangwar@gmail.com"></a>shivamxgangwar@gmail.com</p>
    <p>LinkedIn: <a href="https://www.linkedin.com/in/shivam-gangwar" target="_blank">https://www.linkedin.com/in/shivam-gangwar</a></p>
    <p>GitHub: <a href="https://github.com/Shivamxgangwar" target="_blank">https://github.com/Shivamxgangwar</a></p>
  </section>

  <footer>
    <p>© 2025 Your Name. All Rights Reserved.</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}

body {
  color: #333;
  line-height: 1.6;
  scroll-behavior: smooth;
}

/* ===== Navigation ===== */
header {
  background: #222;
  color: #fff;
  padding: 1rem 2rem;
  position: sticky;
  top: 0;
  z-index: 1000;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 1rem;
}

.nav-links a {
  color: #fff;
  text-decoration: none;
  transition: color 0.3s;
}

.nav-links a:hover {
  color: #00adb5;
}

/* ===== Hero Section ===== */
#hero {
  background: linear-gradient(135deg, #00adb5, #393e46);
  color: white;
  text-align: center;
  padding: 5rem 2rem;
}

.profile-pic {
  width: 180px;
  height: 120px;
  border-radius: 50%;
  border: 3px solid white;
  margin-bottom: 1rem;
  object-fit: cover;
  box-shadow: 0 0 15px rgba(255, 255, 255, 0.3);
}

#hero h2 span {
  color: #fff;
  font-weight: bold;
}

.btn {
  background: #fff;
  color: #00adb5;
  padding: 0.7rem 1.3rem;
  border-radius: 5px;
  text-decoration: none;
  transition: 0.3s;
  display: inline-block;
  margin-top: 1rem;
}

.btn:hover {
  background: #393e46;
  color: #fff;
}

/* ===== Sections ===== */
section {
  padding: 4rem 2rem;
  max-width: 1000px;
  margin: auto;
}

h2 {
  text-align: center;
  color: #00adb5;
  margin-bottom: 2rem;
}

// Simple fade-in animation
const sections = document.querySelectorAll("section");

const observer = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add("fade-in");
    }
  });
});

sections.forEach(section => observer.observe(section));
