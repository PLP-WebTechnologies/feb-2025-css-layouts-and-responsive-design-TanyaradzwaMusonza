# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨

📄 index.html – With Navigation Bar and Layout
html
Copy
Edit

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Styled Page</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <!-- Navigation Bar -->
  <nav class="navbar">
    <div class="nav-brand">MySite</div>
    <ul class="nav-links">
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>

  <!-- Main Content Grid -->
  <main class="main-grid">
    <section class="content">
      <h1 class="title">Welcome to My Page</h1>
      <p id="intro">This is a sample paragraph with custom styling.</p>
      <img src="https://via.placeholder.com/300" alt="Example Image" class="styled-image" />
      <div class="content-box">
        <p>This box is styled with margins, padding, and borders.</p>
      </div>
    </section>
    <aside class="sidebar">
      <p>Sidebar Content</p>
    </aside>
  </main>
</body>
</html>
🎨 style.css – With Flexbox, Grid & Media Queries
css
Copy
Edit

/* Base Styles */
body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: #f4f4f9;
  margin: 0;
  padding: 0;
}

/* Navbar using Flexbox */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #2c3e50;
  color: white;
  padding: 1rem;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 1rem;
}

.nav-links a {
  color: white;
  text-decoration: none;
}

/* Main content layout using CSS Grid */
.main-grid {
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: 20px;
  padding: 20px;
}

.content {
  background-color: #fff;
  padding: 20px;
  border-radius: 10px;
}

.sidebar {
  background-color: #ecf0f1;
  padding: 20px;
  border-radius: 10px;
}

/* Typography and Styling */
.title {
  color: #2c3e50;
  font-size: 2em;
  text-align: center;
  margin-bottom: 10px;
}

#intro {
  color: #34495e;
  font-size: 1.1em;
  padding: 10px;
  background-color: #eaf2f8;
  border-left: 4px solid #2980b9;
}

.styled-image {
  display: block;
  width: 100%;
  max-width: 300px;
  margin: 20px auto;
  padding: 10px;
  border: 5px solid #3498db;
  border-radius: 10px;
}

.content-box {
  background-color: #ffffff;
  border: 2px solid #bdc3c7;
  padding: 15px;
  margin-top: 20px;
  font-family: Georgia, serif;
  font-size: 1em;
}

/* 🌐 Responsive Design with Media Queries */
@media (max-width: 768px) {
  .main-grid {
    grid-template-columns: 1fr;
  }

  .nav-links {
    flex-direction: column;
    gap: 0.5rem;
  }
}

@media (max-width: 480px) {
  .navbar {
    flex-direction: column;
    align-items: flex-start;
  }

  .main-grid {
    padding: 10px;
  }

  .content, .sidebar {
    padding: 15px;
  }
}

