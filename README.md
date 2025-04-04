<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Database Project - Space Theme</title>
  <link href="https://fonts.googleapis.com/css2?family=MedievalSharp&family=Crimson+Text&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Quicksand', sans-serif;
      background: linear-gradient(135deg, #0b002b, #140044, #1a003e);
      color: white;
      padding: 2rem;
      perspective: 1000px;
      overflow-x: hidden;
    }

    body::before {
      content: '';
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-image: 
        radial-gradient(circle, rgba(100, 100, 100, 0.1) 1px, transparent 1px),
        radial-gradient(circle, rgba(80, 80, 80, 0.05) 2px, transparent 2px);
      background-size: 50px 50px, 100px 100px;
      z-index: -1;
      opacity: 0.3;
    }

    h1, h2 {
      font-family: 'Orbitron', sans-serif;
      text-align: center;
      text-shadow: 0 0 20px #ff69b4;
      color: #ff69b4;
    }

    h1 {
      font-size: 2.5rem;
      margin-bottom: 2rem;
    }

    .content {
      transform-style: preserve-3d;
      transition: transform 0.8s ease-in-out;
    }
    
    .content.clicked {
     transform: rotateY(10deg) rotateX(3deg) scale(1.02);
    }

    .table-container {
      margin: 2rem auto;
      max-width: 800px;
      background: rgba(255, 255, 255, 0.05);
      box-shadow: 0 8px 32px rgba(0, 0, 0, 0.37);
      border-radius: 16px;
      overflow: hidden;
      backdrop-filter: blur(10px);
      transform-style: preserve-3d;
      transition: all 0.5s ease-in-out;
      border: 1px solid rgba(255, 255, 255, 0.2);
    }

    h3 {
      text-align: center;
      color: #b57edc;
      font-family: 'MedievalSharp', cursive;
      margin: 1rem 0;
      letter-spacing: 1px;
    }

    table {
      width: 100%;
      border-collapse: collapse;
    }

    th, td {
      padding: 1rem;
      text-align: left;
      border-bottom: 1px solid rgba(255, 255, 255, 0.2);
    }

    th {
      background: rgba(255, 255, 255, 0.1);
      color: #80b3ff;
    }

    tr {
      transition: background-color 0.3s ease;
    }

    tr:hover {
      background: #4b0082;
    }

    code {
      color: #b57edc;
      background-color: #1a003e;
      padding: 0.2rem 0.5rem;
      border-radius: 4px;
      border: 1px solid #3d3d3d;
    }

    .card {
      margin: 2rem auto;
      max-width: 800px;
      background: #1a003e;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
      border-radius: 8px;
      padding: 1.5rem;
      border: 1px solid #3d3d3d;
    }

    strong {
      color: #ff69b4;
    }

    .key-reflection {
      font-family: 'Crimson Text', serif;
      background: #1a003e;
      color: #d0c0ff;
      padding: 1.5rem;
      margin-top: 2rem;
      border-radius: 8px;
      position: relative;
      border: 1px solid #3d3d3d;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.4);
    }
  
table {
  width: 100%;
  border-collapse: collapse;
  background-color: rgba(255, 255, 255, 0.05);
  color: #ffffff;
}

th, td {
  padding: 1rem;
  text-align: left;
  border-bottom: 1px solid rgba(255, 255, 255, 0.2);
  color: #f0eaff;
}

th {
  background-color: rgba(128, 179, 255, 0.2);
  color: #80b3ff;
}

tr:hover {
  background-color: rgba(75, 0, 130, 0.4);
}

body {
  background-color: #0b002b;
  color: white;
}

</style>
</head>
<body>
  <div class="content" id="content">
    <h1>Database Project</h1>

    <h2>Primary Key Tables</h2>
    <div class="table-container">
      <h3>Authors Table</h3>
      <table>
        <tr><th>Author</th><th>Author ID</th><th>Nationality</th><th>Language</th></tr>
        <tr><td>Jane Austen</td><td>1</td><td>British</td><td>English</td></tr>
        <tr><td>Herman Melville</td><td>2</td><td>American</td><td>English</td></tr>
        <tr><td>George Orwell</td><td>3</td><td>British</td><td>English</td></tr>
        <tr><td>Harper Lee</td><td>4</td><td>American</td><td>English</td></tr>
        <tr><td>F. Scott Fitzgerald</td><td>5</td><td>American</td><td>English</td></tr>
      </table>
    </div>

    <div class="table-container">
      <h3>Checkouts Table</h3>
      <table>
        <tr><th>Checkout ID</th><th>Book ID</th><th>Checkout Date</th><th>Member ID</th></tr>
        <tr><td>101</td><td>1</td><td>2024-03-15</td><td>201</td></tr>
        <tr><td>102</td><td>2</td><td>2024-02-22</td><td>202</td></tr>
        <tr><td>103</td><td>3</td><td>2024-03-01</td><td>203</td></tr>
        <tr><td>104</td><td>4</td><td>2024-03-10</td><td>204</td></tr>
        <tr><td>105</td><td>5</td><td>2024-02-28</td><td>205</td></tr>
      </table>
    </div>

    <h2>Primary Keys Analysis</h2>
    <div class="key-reflection">
      <p>Looking at these database tables, I can see the importance of primary keys in establishing unique identifiers. The Authors table uses Author ID as its primary key, which allows for efficient reference and prevents duplicate entries. Each author is assigned a unique numeric identifier.</p>
      <p>In the Checkouts table, we have Checkout ID as the primary key, with Book ID and Member ID serving as foreign keys that link to other tables. The primary key ensures each checkout record can be uniquely identified in the system.</p>
      <p>Primary keys are fundamental to database design because they enforce entity integrity. Without them, it would be difficult to maintain data consistency or create proper relationships between tables. In this database structure, the primary keys enable us to track which books are checked out by which members without ambiguity.</p>
    </div>
  </div>

  <script>
    // Subtle ambient floating dust particles
    function createDustParticles() {
      for (let i = 0; i < 15; i++) {
        const element = document.createElement('div');
        element.style.position = 'fixed';
        element.style.width = `${Math.random() * 3 + 1}px`;
        element.style.height = element.style.width;
        element.style.backgroundColor = '#b57edc';
        element.style.borderRadius = '50%';
        element.style.opacity = Math.random() * 0.2 + 0.05;
        element.style.left = `${Math.random() * 100}vw`;
        element.style.top = `${Math.random() * 100}vh`;
        element.style.zIndex = '-1';
        
        // Add very subtle animation
        element.style.animation = `float ${Math.random() * 30 + 20}s infinite alternate ease-in-out`;
        
        // Create keyframes for each element with minimal movement
        const keyframes = `
          @keyframes float {
            0% { transform: translate(0, 0); }
            100% { transform: translate(${Math.random() * 40 - 20}px, ${Math.random() * 40 - 20}px); }
          }
        `;
        
        const styleElement = document.createElement('style');
        styleElement.innerHTML = keyframes;
        document.head.appendChild(styleElement);
        
        document.body.appendChild(element);
      }
    }
    
    // Very subtle mouse movement effect - much less rotation
    document.addEventListener('mousemove', function(e) {
      const content = document.getElementById('content');
      const xAxis = (window.innerWidth / 2 - e.pageX) / 150;
      const yAxis = (window.innerHeight / 2 - e.pageY) / 150;
      content.style.transform = `rotateY(${xAxis}deg) rotateX(${yAxis}deg)`;
    });
    
    // Return to normal position when mouse leaves
    document.addEventListener('mouseleave', function() {
      const content = document.getElementById('content');
      content.style.transform = 'rotateY(0deg) rotateX(0deg)';
    });
    
    // Initialize
    window.onload = function() {
      createDustParticles();
    };
    
    document.getElementById('content').addEventListener('click', function() {
      this.classList.toggle('clicked');
    });
  </script>
</body>
</html>
