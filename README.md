# Kaviyan<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Random Quote Generator</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <div class="container">
    <h1>Random Quote Generator</h1>
    <div class="quote-box">
      <p id="quote">Click the button to get inspired!</p>
      <p id="author">—</p>
    </div>
    <button onclick="generateQuote()">New Quote</button>
  </div>
  <script src="script.js"></script>
</body>
</html>body {
  font-family: Arial, sans-serif;
  background: #f4f4f4;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.container {
  text-align: center;
  padding: 20px;
  background: white;
  border-radius: 12px;
  box-shadow: 0 0 15px rgba(0,0,0,0.2);
}

.quote-box {
  margin: 20px 0;
  font-size: 1.2em;
  color: #333;
}

button {
  padding: 10px 20px;
  font-size: 1em;
  border: none;
  background-color: #007BFF;
  color: white;
  border-radius: 8px;
  cursor: pointer;
}

button:hover {
  background-color: #0056b3;
}const quotes = [
  { text: "The best way to get started is to quit talking and begin doing.", author: "Walt Disney" },
  { text: "Don’t let yesterday take up too much of today.", author: "Will Rogers" },
  { text: "It’s not whether you get knocked down, it’s whether you get up.", author: "Vince Lombardi" },
  { text: "Your time is limited, so don’t waste it living someone else’s life.", author: "Steve Jobs" },
  { text: "If you can dream it, you can do it.", author: "Walt Disney" },
  { text: "Believe you can and you’re halfway there.", author: "Theodore Roosevelt" }
];

function generateQuote() {
  const randomIndex = Math.floor(Math.random() * quotes.length);
  const quote = quotes[randomIndex];

  document.getElementById('quote').textContent = `"${quote.text}"`;
  document.getElementById('author').textContent = `— ${quote.author}`;
}

// Generate a quote on page load
window.onload = generateQuote;
