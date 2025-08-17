<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Static Website</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
      scroll-behavior: smooth;
    }

    body {
      background: #f9f9f9;
      color: #333;
    }

    /* Navbar */
    nav {
      width: 100%;
      background: #222;
      color: white;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 15px 30px;
      position: fixed;
      top: 0;
      left: 0;
      z-index: 1000;
    }

    .logo {
      font-size: 22px;
      font-weight: bold;
    }

    .menu {
      list-style: none;
      display: flex;
      gap: 25px;
    }

    .menu a {
      text-decoration: none;
      color: white;
      font-size: 16px;
      transition: 0.3s;
    }

    .menu a:hover {
      color: #00adb5;
    }

    /* Hamburger */
    .hamburger {
      display: none;
      flex-direction: column;
      cursor: pointer;
    }
    .hamburger div {
      width: 25px;
      height: 3px;
      background: white;
      margin: 5px 0;
      transition: 0.3s;
    }

    /* Sections */
    section {
      min-height: 100vh;
      padding: 100px 30px 50px;
    }

    #home {
      background: linear-gradient(to right, #00adb5, #393e46);
      color: white;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      text-align: center;
    }

    #about {
      background: #f5f5f5;
    }

    #services {
      background: #e8f0f2;
    }

    #contact {
      background: #f5f5f5;
    }

    h1, h2 {
      margin-bottom: 20px;
    }

    .services-container {
      display: flex;
      gap: 20px;
      flex-wrap: wrap;
    }

    .service-box {
      flex: 1;
      min-width: 250px;
      background: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0px 2px 6px rgba(0,0,0,0.1);
      text-align: center;
    }

    /* Contact Section */
    .contact-info {
      margin-top: 20px;
      display: flex;
      gap: 30px;
      flex-wrap: wrap;
    }

    .contact-details {
      flex: 1;
      min-width: 250px;
    }

    iframe {
      width: 100%;
      height: 300px;
      border: none;
      border-radius: 10px;
    }

    /* WhatsApp Button */
    .whatsapp-btn {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background: #25d366;
      color: white;
      padding: 12px 18px;
      border-radius: 50px;
      text-decoration: none;
      font-size: 16px;
      display: flex;
      align-items: center;
      gap: 8px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    }
    .whatsapp-btn:hover {
      background: #1ebe57;
    }

    /* Responsive */
    @media (max-width: 768px) {
      .menu {
        position: absolute;
        top: 60px;
        right: -100%;
        background: #222;
        flex-direction: column;
        width: 200px;
        padding: 20px;
        transition: right 0.3s ease;
      }
      .menu.active {
        right: 0;
      }
      .hamburger {
        display: flex;
      }
    }
  </style>
</head>
<body>

  <!-- Navbar -->
  <nav>
    <div class="logo">MyLogo</div>
    <ul class="menu">
      <li><a href="#home">HOME</a></li>
      <li><a href="#about">ABOUT US</a></li>
      <li><a href="#services">SERVICES</a></li>
      <li><a href="#contact">CONTACT US</a></li>
    </ul>
    <div class="hamburger" onclick="toggleMenu()">
      <div></div>
      <div></div>
      <div></div>
    </div>
  </nav>

  <!-- Home -->
  <section id="home">
    <h1>Welcome to My Website</h1>
    <p>We provide amazing services to help you grow.</p>
  </section>

  <!-- About -->
  <section id="about">
    <h2>About Us</h2>
    <p>
      This is an introduction about the website.  
      You can write about your business, NGO, or portfolio here.
    </p>
  </section>

  <!-- Services -->
  <section id="services">
    <h2>Our Services</h2>
    <div class="services-container">
      <div class="service-box">
        <h3>Service 1</h3>
        <p>Description of service 1.</p>
      </div>
      <div class="service-box">
        <h3>Service 2</h3>
        <p>Description of service 2.</p>
      </div>
      <div class="service-box">
        <h3>Service 3</h3>
        <p>Description of service 3.</p>
      </div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact">
    <h2>Contact Us</h2>
    <div class="contact-info">
      <div class="contact-details">
        <p><strong>Address:</strong> Your Address Here</p>
        <p><strong>Email:</strong> example@email.com</p>
        <p><strong>Phone:</strong> +91 9876543210</p>
      </div>
      <div class="contact-map">
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3680.1523209374286!2d72.87765531542648!3d22.56262718519292!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x395e84f8bff4b4f7%3A0xf8c1bb4ddc8b2047!2sGujarat!5e0!3m2!1sen!2sin!4v1673500000000!5m2!1sen!2sin" allowfullscreen="" loading="lazy"></iframe>
      </div>
    </div>
  </section>

  <!-- WhatsApp -->
  <a class="whatsapp-btn" href="https://wa.me/919876543210" target="_blank">
    💬 WhatsApp
  </a>

  <!-- JS -->
  <script>
    function toggleMenu() {
      document.querySelector(".menu").classList.toggle("active");
    }
  </script>

</body>
</html>
