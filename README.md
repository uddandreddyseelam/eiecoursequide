<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>ELECTRONICS INSTRUMENTATION Engineering</title>
  <style>
    /* Global Styles */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #ffffff;
      color: #333333;
      line-height: 1.6;
      padding: 20px;
    }
    h1, h2, h3 {
      color: #0056b3;
    }

    /* Layout Container */
    .container {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      max-width: 1200px;
      margin: 0 auto 30px auto; /* bottom margin for contact */
    }

    /* Sidebar Left */
    .sidebar-left {
      flex: 1 1 250px;
      background-color: #f8f9fa;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
      min-width: 200px;
    }
    .sidebar-left h3 {
      margin-bottom: 15px;
    }
    .sidebar-left p {
      margin-bottom: 15px;
    }

    /* Center Area */
    .center {
      flex: 1 1 500px;
      min-width: 300px;
      display: flex;
      flex-direction: column;
    }
    /* Header area for Latest Posts and menu button */
    .center-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 20px;
    }
    .center-header h2 {
      margin: 0;
    }

    .posts-container {
      display: flex;
      flex-direction: column;
      gap: 15px;
    }
    .post-card {
      background-color: #f8f9fa;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
      transition: transform 0.2s ease, box-shadow 0.2s ease;
    }
    .post-card:hover {
      transform: translateY(-2px);
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.15);
    }
    .post-card h4 {
      margin-bottom: 10px;
      color: #007bff;
    }
    .post-card p {
      color: #555;
    }

    /* Right Sidebar - removed as menu moved */
    .sidebar-right {
      flex: 1 1 200px;
      min-width: 100px;
      /* hidden since menu moved */
      display: none;
    }

    /* Menu button inside center header */
    .menu-btn {
      background: none;
      border: none;
      font-size: 24px;
      cursor: pointer;
      padding: 10px;
      border-radius: 4px;
      transition: background-color 0.2s ease;
      line-height: 1;
    }
    .menu-btn:hover {
      background-color: #e9ecef;
    }

    .dropdown {
      position: absolute;
      top: 60px; /* below the menu button */
      right: 20px; /* align with container right */
      background-color: #ffffff;
      border: 1px solid #ddd;
      border-radius: 8px;
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
      width: 280px;
      z-index: 1000;
      display: none;
      padding: 15px 20px;
    }
    .dropdown.show {
      display: block;
    }
    .dropdown ul {
      list-style: none;
      padding-left: 0;
    }
    .dropdown li {
      margin-bottom: 15px;
    }
    .dropdown li strong {
      display: block;
      margin-bottom: 8px;
      font-size: 1.1rem;
      color: #0056b3;
    }
    .dropdown li ul {
      list-style: decimal inside;
      padding-left: 15px;
      margin-top: 5px;
    }
    .dropdown li ul li {
      margin-bottom: 6px;
    }
    .dropdown li a {
      color: #333;
      text-decoration: none;
      transition: color 0.2s ease;
    }
    .dropdown li a:hover {
      color: #007bff;
      text-decoration: underline;
    }

    /* Contact Section */
    .contact-section {
      max-width: 1200px;
      margin: 0 auto;
      background-color: #f8f9fa;
      padding: 30px;
      border-radius: 8px;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
      text-align: center;
    }
    .contact-section h2 {
      margin-bottom: 20px;
    }
    .contact-details {
      font-size: 1.1rem;
    }
    .contact-details p {
      margin-bottom: 10px;
    }
    .contact-details a {
      color: #007bff;
      text-decoration: none;
    }
    .contact-details a:hover {
      text-decoration: underline;
    }

    /* Mobile Responsiveness */
    @media (max-width: 768px) {
      .container {
        flex-direction: column;
      }
      .sidebar-left, .center, .sidebar-right {
        flex: 1 1 100%;
        margin-bottom: 20px;
      }
      .sidebar-right {
        display: none;
      }
      .contact-section {
        padding: 20px;
      }
      .center-header {
        position: relative;
      }
      .dropdown {
        top: 50px;
        right: 10px;
        width: 90vw;
        max-width: 320px;
        padding: 15px;
      }
    }

    /* Header */
    .header {
      text-align: center;
      margin-bottom: 30px;
    }
    .header h1 {
      font-size: 2.5rem;
      margin-bottom: 10px;
    }
  </style>
</head>
<body>
  <!-- Main Header -->
  <div class="header">
    <h1>Electronics Instrumentation Engineering</h1>
    <p>Your go-to resource for syllabus updates and educational information based on EIE.</p>
  </div>

  <!-- Main Layout Container -->
  <div class="container">
    <!-- Left Sidebar -->
    <aside class="sidebar-left">
      <h3>About the Site</h3>
      <p>This website provides up-to-date syllabus information for various courses in Electrical and Instrumentation Engineering. Stay informed with the latest updates.</p>
      <h3>About the Authors</h3>
      <p>Developed by a team of educators and engineers dedicated to helping students succeed.</p>
    </aside>

    <!-- Center Area: Latest Posts + Menu -->
    <main class="center">
      <div class="center-header">
        <h2>Latest Posts</h2>
        <button class="menu-btn" id="menuBtn" aria-label="Open menu">⋮</button>
        <div class="dropdown" id="dropdownMenu" role="menu" aria-hidden="true">
          <ul>
            <li>
              <strong>Diploma Courses</strong>
              <ul>
                <li><a href="#diploma">Diploma</a></li>
                <li><a href="#diploma-eie">EIE</a></li>
                <li><a href="#diploma-csiot">CSIOT</a></li>
              </ul>
            </li>
            <li>
              <strong>B.Tech Courses</strong>
              <ul>
                <li><a href="#btech">B.Tech</a></li>
                <li><a href="#btech-eie">EIE</a></li>
                <li><a href="#btech-industrial">Industrial Instrumentation</a></li>
              </ul>
            </li>
            <li>
              <strong>College Details</strong>
              <ul>
                <li>VIGNAN INSTITUTE OF TECHNOLOGY AND SCIENCE</li>
                <li>Address: [Add Address Here]</li>
                <li>Phone: [Add Phone Number]</li>
                <li>Email: <a href="mailto:contact@vignanits.edu">contact@vignanits.edu</a></li>
                <li>Website: <a href="https://www.vignanits.ac.in" target="_blank" rel="noopener">www.vignanits.ac.in</a></li>
              </ul>
            </li>
            <li><a href="#about-website">About Website</a></li>
            <li><a href="#contact-us">Contact Us</a></li>
          </ul>
        </div>
      </div>
      <div id="posts" class="posts-container">
        <!-- Posts will be dynamically loaded here -->
      </div>
    </main>

    <!-- Right Sidebar: removed since menu moved -->
    <aside class="sidebar-right"></aside>
  </div>

  <!-- Contact Section -->
  <section id="contact-us" class="contact-section">
    <h2>Contact Us</h2>
    <div class="contact-details">
      <p><strong>Name:</strong> Seelam Uddand Reddy</p>
      <p><strong>Email:</strong> <a href="mailto:uddandreddyseelam@gmail.com">uddandreddyseelam@gmail.com</a></p>
      <p>If you have any questions or need assistance, feel free to reach out to us!</p>
    </div>
  </section>

  <!-- JavaScript for Dynamic Posts and Menu Toggle -->
  <script>
    // Data for Latest Posts - Easy to update by modifying this array
    const latestPosts = [
      {
        title: "Diploma 2025 Updated Syllabus",
        description: "New revisions include advanced circuits and programming modules. Download the latest syllabus here."
      },
      {
        title: "B.Tech Semester 3 Syllabus Updated",
        description: "Updates focus on data structures, algorithms, and electrical fundamentals. Check for changes."
      },
      {
        title: "New Elective Options for EIE Students",
        description: "Explore emerging subjects like IoT and renewable energy integrations."
      }
    ];

    // Function to render posts dynamically
    function renderPosts() {
      const postsContainer = document.getElementById('posts');
      latestPosts.forEach(post => {
        const postCard = document.createElement('div');
        postCard.className = 'post-card';
        postCard.innerHTML = `
          <h4>${post.title}</h4>
          <p>${post.description}</p>
        `;
        postsContainer.appendChild(postCard);
      });
    }

    // Menu Toggle Functionality
    const menuBtn = document.getElementById('menuBtn');
    const dropdownMenu = document.getElementById('dropdownMenu');

    menuBtn.addEventListener('click', () => {
      const isShown = dropdownMenu.classList.toggle('show');
      dropdownMenu.setAttribute('aria-hidden', !isShown);
    });

    // Close menu when clicking outside
    document.addEventListener('click', (event) => {
      if (!menuBtn.contains(event.target) && !dropdownMenu.contains(event.target)) {
        dropdownMenu.classList.remove('show');
        dropdownMenu.setAttribute('aria-hidden', 'true');
      }
    });

    // Initialize the page by rendering posts
    document.addEventListener('DOMContentLoaded', renderPosts);
  </script>
</body>
</html>
