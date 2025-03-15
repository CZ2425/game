# game
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Number Guessing Game</title>
</head>
<body>
  <h1>Number Guessing Game</h1>
  <p>Guess a number between 1 and 10:</p>
  <input type="number" id="guessInput" min="1" max="10">
  <button onclick="checkGuess()">Guess</button>
  <p id="result"></p>

  <script>
    // Generate a random number between 1 and 10
    const secretNumber = Math.floor(Math.random() * 10) + 1;

    function checkGuess() {
      const guess = Number(document.getElementById('guessInput').value);
      const result = document.getElementById('result');

      if (guess === secretNumber) {
        result.textContent = "Congratulations! You guessed it right!";
      } else if (guess < secretNumber) {
        result.textContent = "Too low! Try a higher number.";
      } else {
        result.textContent = "Too high! Try a lower number.";
      }
    }
  </script>
</body>
</html>
