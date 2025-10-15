<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Wedding Anniversary Login</title>
  <style>
    * {
      box-sizing: border-box;
    }
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to right, #ffecd2, #fcb69f);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
    }
    .container {
      width: 100%;
      max-width: 400px;
      padding: 20px;
      background: white;
      border-radius: 15px;
      box-shadow: 0 0 20px rgba(0,0,0,0.2);
      text-align: center;
      animation: fadeIn 1s ease-in;
    }
    input {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border: 2px solid #ccc;
      border-radius: 8px;
      font-size: 1em;
    }
    button {
      width: 100%;
      padding: 10px;
      background: #e91e63;
      color: white;
      border: none;
      border-radius: 8px;
      font-size: 1em;
      cursor: pointer;
      transition: background 0.3s ease;
    }
    button:hover {
      background: #d81b60;
    }
    #error {
      color: red;
      font-size: 0.9em;
    }

    .card {
      display: none;
      flex-direction: column;
      align-items: center;
      animation: fadeIn 1s ease-in;
    }
    .card h1 {
      color: #e91e63;
      font-size: 2em;
      margin-bottom: 10px;
      animation: bounce 1.5s infinite;
    }
    .card .names {
      font-size: 1.5em;
      margin: 10px 0;
      color: #333;
    }
    .card p {
      font-size: 1.1em;
      color: #555;
    }
    .hearts {
      font-size: 2em;
      color: red;
      animation: pulse 1s infinite;
      margin-top: 10px;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: scale(0.9); }
      to { opacity: 1; transform: scale(1); }
    }
    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.2); }
      100% { transform: scale(1); }
    }
    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }
  </style>
</head>
<body>
  <div class="container" id="loginBox">
    <h2>Login</h2>
    <input type="text" id="username" placeholder="Username" />
    <input type="password" id="password" placeholder="Password" />
    <button onclick="login()">Login</button>
    <p id="error"></p>
  </div>

  <div class="container card" id="cardBox">
    <h1>Happy Wedding Anniversary!</h1>
    <div class="names">💖 G Vinay & Haripriya (Bujji) 💖</div>
    <p>Wishing you both a lifetime of love, laughter, and happiness!</p>
    <div class="hearts">❤️❤️❤️</div>
  </div>

  <script>
    function login() {
      const user = document.getElementById('username').value;
      const pass = document.getElementById('password').value;
      if (user === pass && user !== "") {
        document.getElementById('loginBox').style.display = 'none';
        document.getElementById('cardBox').style.display = 'flex';
      } else {
        document.getElementById('error').textContent = "Username and password must match!";
      }
    }
  </script>
</body>
</html>
