<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Renter's Return</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 0;
      padding: 0;
      color: #333;
      background-color: #ffffff;
    }
    header {
      background-color: #0A1F44;
      color: white;
      padding: 20px 40px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    header h2 {
      margin: 0;
      font-size: 1.8em;
    }
    nav a {
      color: white;
      margin: 0 15px;
      text-decoration: none;
      font-weight: 600;
    }
    .hero {
      padding: 80px 40px;
      background-color: #F2F4F8;
      text-align: center;
    }
    .hero h1 {
      font-size: 3em;
      margin-bottom: 20px;
    }
    .hero p {
      font-size: 1.2em;
      color: #555;
    }
    .cta-btn {
      display: inline-block;
      margin-top: 30px;
      padding: 12px 30px;
      background-color: #0A1F44;
      color: white;
      text-decoration: none;
      font-weight: bold;
      border-radius: 8px;
    }
    .section {
      padding: 60px 40px;
      max-width: 1000px;
      margin: auto;
    }
    .features {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
      gap: 30px;
    }
    .feature-item {
      background-color: #f9f9f9;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }
    .calculator {
      background-color: #f2f2f2;
      padding: 40px;
      border-radius: 8px;
      max-width: 600px;
      margin: 0 auto 60px;
    }
    .calculator h2 {
      margin-top: 0;
    }
    .calculator input {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border-radius: 4px;
      border: 1px solid #ccc;
    }
    .calculator button {
      background-color: #0A1F44;
      color: white;
      border: none;
      padding: 10px 20px;
      border-radius: 6px;
      cursor: pointer;
    }
    .calculator p.result {
      margin-top: 20px;
      font-weight: bold;
    }
    .footer {
      background-color: #0A1F44;
      color: white;
      text-align: center;
      padding: 20px;
      margin-top: 40px;
    }
  </style>
</head>
<body>
  <header>
    <h2>Renter's Return</h2>
    <nav>
      <a href="#">Home</a>
      <a href="#how">How It Works</a>
      <a href="#calculator">Calculator</a>
      <a href="#about">About</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section class="hero">
    <h1>Turn NYC Real Estate Numbers Into Smart Investment Decisions</h1>
    <p>Calculate cash flow, cap rate, and ROI across all 5 boroughs—clearly and confidently.</p>
    <a href="#calculator" class="cta-btn">Try the Calculator</a>
  </section>

  <section class="section" id="why">
    <h2>Why We Built Renter's Return</h2>
    <p>
      Navigating New York City's real estate market is tough—even for professionals.
      With taxes, HOA fees, maintenance costs, and rent estimates varying by borough,
      it's easy to misjudge a property’s true profitability.
    </p>
    <p>
      That’s where Renter’s Return comes in.
      This tool was created by someone who experienced firsthand how time-consuming
      and confusing it is to estimate returns across NYC properties.
    </p>
    <p>
      Instead of juggling spreadsheets and rough estimates, Renter’s Return gives you
      clean, fast, and accurate insights for smarter investing—no finance degree required.
    </p>
  </section>

  <section class="section">
    <h2>Key Features</h2>
    <div class="features">
      <div class="feature-item">
        <h3>📍 Borough-based Rent Estimates</h3>
        <p>Get realistic rental income projections for all five NYC boroughs.</p>
      </div>
      <div class="feature-item">
        <h3>💰 Investment Metrics</h3>
        <p>Instant calculations for Cap Rate, Cash-on-Cash Return, NOI, and more.</p>
      </div>
      <div class="feature-item">
        <h3>📈 Scenario Planning</h3>
        <p>Customize expenses, maintenance, and rent growth to simulate different outcomes.</p>
      </div>
      <div class="feature-item">
        <h3>📥 Easy & Free to Use</h3>
        <p>No sign-up required. Start analyzing in seconds with our intuitive interface.</p>
      </div>
    </div>
  </section>

  <section class="section calculator" id="calculator">
    <h2>Try the Calculator (with Example)</h2>
    <form onsubmit="event.preventDefault(); calculateCapRate();">
      <label>Annual Rental Income ($):</label>
      <input type="number" id="income" value="48000">
      <label>Annual Expenses ($):</label>
      <input type="number" id="expenses" value="15000">
      <label>Property Price ($):</label>
      <input type="number" id="price" value="600000">
      <button type="submit">Calculate Cap Rate</button>
    </form>
    <p class="result" id="result"></p>
  </section>

  <div class="footer">
    <p>&copy; 2025 Renter's Return. All rights reserved.</p>
  </div>

  <script>
    function calculateCapRate() {
      const income = parseFloat(document.getElementById('income').value);
      const expenses = parseFloat(document.getElementById('expenses').value);
      const price = parseFloat(document.getElementById('price').value);
      const netIncome = income - expenses;
      const capRate = ((netIncome / price) * 100).toFixed(2);
      document.getElementById('result').innerText = `Cap Rate: ${capRate}%`;
    }
  </script>
</body>
</html>
