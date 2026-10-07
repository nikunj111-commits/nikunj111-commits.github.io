<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Nikunj's Website</title>

  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f1f5f9;
      color: #222;
      text-align: center;
    }

    header {
      background: #1769aa;
      color: white;
      padding: 40px 20px;
    }

    main {
      max-width: 700px;
      margin: 30px auto;
      padding: 25px;
      background: white;
      border-radius: 12px;
    }

    button {
      padding: 12px 20px;
      background: #1769aa;
      color: white;
      border: none;
      border-radius: 6px;
      cursor: pointer;
    }

    button:hover {
      background: #0d4f82;
    }
  </style>
</head>

<body>
  <header>
    <h1>Hello, I am Nikunj</h1>
    <p>Welcome to my first website</p>
  </header>

  <main>
    <h2>Welcome to My Website</h2>

    <p>
      Here I will share useful information about Engineering,
      Technology and Learning.
    </p>

    <button onclick="showMessage()">Click Me</button>

    <p id="message"></p>
  </main>

  <script>
    function showMessage() {
      document.getElementById("message").innerText =
        "Thank you for visiting my website!";
    }
  </script>
</body>
</html>