<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Divakar Kummari | Portfolio</title>
  <style>
    /* Reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #f4f7fa;
      color: #333;
      line-height: 1.6;
    }

    header {
      background-color: #0077cc;
      color: #fff;
      padding: 30px 0;
      text-align: center;
    }

    header h1 {
      font-size: 2.8rem;
      margin-bottom: 5px;
    }

    header p {
      font-size: 1.2rem;
      font-weight: 300;
    }

    .container {
      max-width: 900px;
      margin: 40px auto;
      padding: 0 20px;
    }

    section {
      margin-bottom: 50px;
      opacity: 0;
      transform: translateY(30px);
      transition: all 0.6s ease-out;
    }

    section.visible {
      opacity: 1;
      transform: translateY(0);
    }

    h2 {
      font-size: 2rem;
      color: #0077cc;
      margin-bottom: 15px;
      border-bottom: 2px solid #0077cc;
      padding-bottom: 5px;
      width: fit-content;
    }

    /* About Me */
    #about p {
      font-size: 1.1rem;
      color: #555;
    }

    /* Projects */
    .projects-list {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }

    .project-item {
      background: white;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 3px 8px rgba(0, 0, 0, 0.1);
      transition: transform 0.2s ease;
    }

    .project-item:hover {
      transform: translateY(-5px);
    }

    .project-item h3 {
      margin-bottom: 10px;
      color: #0077cc;
    }

    .project-item p {
      font-size: 1rem;
      color: #666;
    }

    /* Skills */
    #skills ul {
      list-style: none;
      display: flex;
      flex-wrap: wrap;
      gap: 15px;
      padding-left: 0;
    }

    #skills li {
      background: #0077cc;
      color: white;
      padding: 10px 15px;
      border-radius: 20px;
      font-weight: 600;
      font-size: 0.9rem;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      user-select: none;
    }

    /* Education */
    #education ul,
    #hobbies ul,
    #contact ul {
      list-style-type: square;
      padding-left: 20px;
      color: #555;
    }

    #education li,
    #hobbies li,
    #contact li {
      margin-bottom: 10px;
      font-size: 1.1rem;
    }

    /* Contact Links */
    #contact a {
      color: #0077cc;
      text-decoration: none;
      font-weight: 600;
    }

    #contact a:hover {
      text-decoration: underline;
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 20px 0;
      background-color: #0077cc;
      color: white;
      font-size: 0.9rem;
      margin-top: 40px;
    }

    /* Responsive */
    @media (max-width: 600px) {
      header h1 {
        font-size: 2rem;
      }

      h2 {
        font-size: 1.6rem;
      }

      #skills ul {
        justify-content: center;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>Divakar Kummari</h1>
    <p>Web Developer | Programmer | Designer</p>
  </header>

  <div class="container">
    
    <!-- ABOUT -->
    <section id="about" class="reveal">
      <h2>About Me</h2>
      <p>
        Hi! I'm Divakar, a passionate web developer with experience in building modern and responsive websites. I love turning ideas into reality using code and design.
      </p>
    </section>

    <!-- PROJECTS -->
    <section id="projects" class="reveal">
      <h2>Projects</h2>
      <div class="projects-list">
        <div class="project-item">
          <h3>Personal Portfolio Website</h3>
          <p>A clean and responsive portfolio website to showcase my skills and projects.</p>
        </div>
        <div class="project-item">
          <h3>Todo App</h3>
          <p>A simple and user-friendly todo list app built with JavaScript.</p>
        </div>
        <div class="project-item">
          <h3>Weather App</h3>
          <p>A web app that shows current weather using an external API.</p>
        </div>
      </div>
    </section>

    <!-- SKILLS -->
    <section id="skills" class="reveal">
      <h2>Skills</h2>
      <ul>
        <li>HTML5</li>
        <li>CSS3</li>
        <li>JavaScript</li>
        <li>Git & GitHub</li>
        <li>Responsive Design</li>
      </ul>
    </section>

    <!-- EDUCATION -->
    <section id="education" class="reveal">
      <h2>Education</h2>
      <ul>
        <li>B.Tech in Computer Science - Lovely Professional University (2027)</li>
        <li>Intermediate - Narayana Junior College (2021–2023)</li>
      </ul>
    </section>

    <!-- HOBBIES -->
    <section id="hobbies" class="reveal">
      <h2>Hobbies</h2>
      <ul>
        <li>Reading Books</li>
        <li>Coding & Learning New Technologies</li>
        <li>Photography</li>
        <li>Traveling</li>
      </ul>
    </section>

    <!-- CONTACT -->
    <section id="contact" class="reveal">
      <h2>Contact</h2>
      <ul>
        <li>You can reach me at: 
          <a href="mailto:kummaridiwakar7@gmail.com">kummaridiwakar7@gmail.com</a>
        </li>
        <li>Or connect with me on 
          <a href="https://github.com/kummaridiwakar7" target="_blank">https://github.com/kummaridiwakar7</a>
        </li>
      </ul>
    </section>

  </div>

  <footer>
    &copy; 2025 Divakar Kummari. All rights reserved.
  </footer>

  <script>
    // Simple scroll reveal animation
    function reveal() {
      const reveals = document.querySelectorAll('.reveal');
      for (let i = 0; i < reveals.length; i++) {
        const windowHeight = window.innerHeight;
        const elementTop = reveals[i].getBoundingClientRect().top;
        const revealPoint = 150;
        if (elementTop < windowHeight - revealPoint) {
          reveals[i].classList.add('visible');
        }
      }
    }

    window.addEventListener('scroll', reveal);
    window.addEventListener('load', reveal);
  </script>

</body>
</html>
