# Rock-Paper-Scissors Game

Welcome to the **Rock-Paper-Scissors Game** repository! This project is a simple web application written in HTML, CSS, and JavaScript. The application allows users to play the classic Rock-Paper-Scissors game against the computer.

## Features

- **Classic Gameplay**: Play the traditional Rock-Paper-Scissors game.
- **Computer Opponent**: Play against a computer that randomly selects its moves.
- **Interactive Interface**: Simple and intuitive user interface for easy gameplay.
- **Responsive Design**: Optimized for both desktop and mobile devices.

## Technologies

- **Frontend**: HTML5, CSS3, JavaScript (Vanilla JS)

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/rock-paper-scissors-game.git
   cd rock-paper-scissors-game
   ```

2. **Open the index.html file**:
   - You can open the `index.html` file directly in your web browser to play the Rock-Paper-Scissors game.

## Usage

1. Open the Rock-Paper-Scissors Game in your web browser.
2. Select Rock, Paper, or Scissors to make your move.
3. The computer will randomly select its move, and the winner will be displayed.

## Project Structure

- `index.html`: The main HTML file for the Rock-Paper-Scissors Game.
- `style.css`: CSS file for styling the game interface.
- `script.js`: JavaScript file for handling the game logic and interactions.

## Example

Here’s a simple example of the JavaScript code used to handle the game logic:

```javascript
// Example of game logic
const choices = ['rock', 'paper', 'scissors'];

document.querySelectorAll('.choice').forEach(button => {
  button.addEventListener('click', function() {
    const userChoice = this.id;
    const computerChoice = choices[Math.floor(Math.random() * 3)];
    
    const result = determineWinner(userChoice, computerChoice);
    displayResult(userChoice, computerChoice, result);
  });
});

function determineWinner(userChoice, computerChoice) {
  if (userChoice === computerChoice) {
    return 'draw';
  } else if (
    (userChoice === 'rock' && computerChoice === 'scissors') ||
    (userChoice === 'paper' && computerChoice === 'rock') ||
    (userChoice === 'scissors' && computerChoice === 'paper')
  ) {
    return 'user';
  } else {
    return 'computer';
  }
}

function displayResult(userChoice, computerChoice, result) {
  document.getElementById('userChoice').textContent = `You chose: ${userChoice}`;
  document.getElementById('computerChoice').textContent = `Computer chose: ${computerChoice}`;
  document.getElementById('result').textContent = `Result: ${result === 'draw' ? 'It\'s a draw!' : result === 'user' ? 'You win!' : 'Computer wins!'}`;
}
```

## Contributing

Contributions are welcome! If you have any suggestions or improvements, feel free to submit a pull request. Please ensure your changes align with the project goals and maintain code quality.

## License

This project is licensed under the MIT License – see the [LICENSE.md](LICENSE.md) file for details.
