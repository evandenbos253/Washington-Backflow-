# Washington-Backflow-
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Washington Backflow LLC</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <img src="images/logo.png" alt="Washington Backflow LLC Logo" class="logo">
  </header>
  <nav>
    <input type="checkbox" id="nav-toggle" class="nav-toggle" />
    <label for="nav-toggle" class="nav-toggle-label">&#9776; Menu</label>
    <ul class="navbar">
      <li><a href="#home" class="active">Home</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#contact">Contact</a></li>
      <li><a href="#about">About Us</a></li>
    </ul>
  </nav>
  <main>
    <section id="home">
      <h1>Washington Backflow LLC</h1>
      <p class="tagline">Specializing in Backflow Prevention Assembly Testing & Repairs</p>
    </section>
    <section id="services">
      <h2>Our Services</h2>
      <div class="service-list">
        <div class="service">
          <h3>Backflow Testing</h3>
          <p>
            Ensure your water system meets all safety and compliance regulations. We provide certified testing for all types of backflow prevention assemblies.
          </p>
        </div>
        <div class="service">
          <h3>Backflow Repairs</h3>
          <p>
            Reliable repairs and maintenance to keep your backflow devices functioning properly and prevent costly failures.
          </p>
        </div>
      </div>
    </section>
    <section id="contact">
      <h2>Contact Us</h2>
      <p>
        Ready to schedule a test or repair?<br>
        <a href="mailto:info@washingtonbackflow.com">info@washingtonbackflow.com</a>
      </p>
    </section>
    <section id="about">
      <h2>About Us</h2>
      <p>
        Washington Backflow LLC is dedicated to ensuring safe, compliant water systems in your community. Our certified professionals specialize in the testing and repair of backflow prevention assemblies, delivering reliable and trustworthy service across the region.
      </p>
    </section>
  </main>
  <footer>
    <p>&copy; 2025 Washington Backflow LLC. All rights reserved.</p>
  </footer>
</body>
</html>

:root {
  --primary-blue: #195561;
  --background-tan: #f5efdf;
  --accent-blue: #38B6FF;
}

body {
  font-family: 'Segoe UI', Arial, sans-serif;
  background: var(--background-tan);
  color: var(--primary-blue);
  margin: 0;
  padding: 0;
}

header {
  text-align: center;
  padding: 2rem 1rem 1rem 1rem;
  background: var(--background-tan);
}

.logo {
  width: 160px;
  max-width: 60vw;
  margin-bottom: 0.5rem;
}

nav {
  background-color: var(--primary-blue);
  position: relative;
}

.navbar {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
  transition: max-height 0.3s;
}

.navbar li {
  margin: 0;
}

.navbar a {
  display: block;
  color: var(--background-tan);
  text-decoration: none;
  padding: 1rem 2rem;
  font-weight: 500;
  transition: background 0.2s, color 0.2s;
  border-bottom: 3px solid transparent;
  font-size: 1.1rem;
}

.navbar a.active,
.navbar a:hover,
.navbar a:focus {
  color: var(--accent-blue);
  background: #e2ddd0;
  border-bottom: 3px solid var(--accent-blue);
}

/* Hamburger menu for mobile */
.nav-toggle {
  display: none;
}
.nav-toggle-label {
  display: none;
  font-size: 2rem;
  color: var(--background-tan);
  background: var(--primary-blue);
  padding: 1rem 2rem;
  cursor: pointer;
  user-select: none;
}

main {
  max-width: 850px;
  margin: 2rem auto;
  padding: 0 1rem;
}

section {
  margin-bottom: 2.5rem;
}

h1 {
  margin: 0;
  font-size: 2.2rem;
  color: var(--primary-blue);
}

h2 {
  font-size: 1.6rem;
  margin-top: 0;
  color: var(--primary-blue);
}

.tagline {
  font-size: 1.1rem;
  margin: 0.5rem 0 0 0;
}

.service-list {
  display: flex;
  flex-wrap: wrap;
  gap: 2rem;
  justify-content: center;
}

.service {
  background: #e2ddd0;
  border-radius: 8px;
  padding: 1.5rem;
  min-width: 240px;
  flex: 1 1 300px;
  box-shadow: 0 2px 8px rgba(25,85,97,0.06);
  border-left: 4px solid var(--accent-blue);
}

.service h3 {
  margin-top: 0;
  color: var(--primary-blue);
}

.contact a {
  color: var(--accent-blue);
  text-decoration: underline;
}

footer {
  text-align: center;
  padding: 1rem 0;
  background: #e2ddd0;
  color: var(--primary-blue);
  margin-top: 2rem;
  font-size: 0.95rem;
}

/* Responsive Design */
@media (max-width: 900px) {
  main {
    max-width: 100vw;
    padding: 0 1.5vw;
  }
  .service-list {
    gap: 1.5rem;
  }
}
@media (max-width: 700px) {
  .service-list {
    flex-direction: column;
    gap: 1.2rem;
  }
  .navbar a {
    padding: 1rem 1rem;
    font-size: 1rem;
  }
  .logo {
    width: 120px;
  }
}

/* Enhanced mobile nav */
@media (max-width: 600px) {
  .navbar {
    flex-direction: column;
    max-height: 0;
    overflow: hidden;
    background: var(--primary-blue);
    box-shadow: 0 4px 8px rgba(25,85,97,0.06);
    width: 100%;
    text-align: center;
  }
  .nav-toggle:checked + .nav-toggle-label + .navbar {
    max-height: 400px;
    border-bottom: 1px solid #e2ddd0;
  }
  .nav-toggle-label {
    display: block;
  }
  .navbar a {
    padding: 1rem 0;
    border-bottom: 1px solid #e2ddd0;
    font-size: 1.2rem;
  }
}

/* Touch-friendly tap targets */
@media (hover: none) and (pointer: coarse) {
  .navbar a {
    padding: 1.2rem 0.5rem;
    font-size: 1.2rem;
  }
}