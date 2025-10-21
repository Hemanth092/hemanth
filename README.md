# hemanth
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Row Counter</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background-image: url('https://images.unsplash.com/photo-1486308510493-aa64833634ef?auto=format&fit=crop&w=1200&q=80');
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      height: 100vh;
      margin: 0;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .container {
      background-color: rgba(255, 255, 255, 0.7);
      border-radius: 10px;
      padding: 30px;
      width: 320px;
      box-shadow: 0px 4px 12px rgba(0,0,0,0.3);
    }

    h1 {
      margin-bottom: 10px;
      color: #000;
    }

    #count-el {
      font-size: 48px;
      margin: 10px 0 20px;
      color: black;
    }

    .buttons {
      margin-bottom: 20px;
    }

    #increment-btn {
      background-color: darkred;
      color: white;
      border: none;
      padding: 10px 25px;
      margin-right: 10px;
      font-weight: bold;
      border-radius: 5px;
      cursor: pointer;
    }

    #save-btn {
      background-color: darkgreen;
      color: white;
      border: none;
      padding: 10px 25px;
      font-weight: bold;
      border-radius: 5px;
      cursor: pointer;
    }

    button:hover {
      opacity: 0.8;
    }

    #save-el {
      font-size: 18px;
      color: black;
      margin-top: 10px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Row Counter</h1>
    <h2 id="count-el">0</h2>
    <div class="buttons">
      <button id="increment-btn">INCREMENT</button>
      <button id="save-btn">SAVE</button>
    </div>
    <p id="save-el">Previous entries: </p>
  </div>

  <script>
    let count = 0;
    let countEl = document.getElementById("count-el");
    let saveEl = document.getElementById("save-el");

    document.getElementById("increment-btn").addEventListener("click", function() {
      count += 1;
      countEl.textContent = count;
    });

    document.getElementById("save-btn").addEventListener("click", function() {
      saveEl.textContent += count + " - ";
      count = 0;
      countEl.textContent = count;
    });
  </script>
</body>
</html>

