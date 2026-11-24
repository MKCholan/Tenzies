# Tenzies

An interactive dice game built with [React](https://react.dev/) where players roll ten dice and hold matching values until all dice show the same number.

## Rules & Gameplay

- Roll until all ten dice display the same value.
- Click any die to freeze (`isHeld`) or unfreeze its current value between rolls.
- Click **Roll** to roll only unheld dice.
- Once all dice are held with matching values (`gameWon`), confetti appears, keyboard focus automatically moves to the **New Game** button via a ref, and clicking it starts a fresh round.

## Project Structure

- `index.html` — Root HTML document and page metadata.
- `index.jsx` — Application entry point mounting the root React component.
- `src/App.jsx` (or `App.jsx`) — Manages dice state (`useState`), win condition evaluation, roll/reset logic, confetti rendering, and focus management (`useRef` + `useEffect`).
- `src/Die.jsx` (or `Die.jsx`) — Renders an individual die button with its value, held state styling, and click handler.
- `index.css` — Layout and visual styling for the game board, dice, and action button.

## Dependencies

- `react` (`^18.3.1`)
- `react-dom` (`^18.3.1`)
- `nanoid` (`^5.0.7`) — Generates unique IDs for each die.
- `react-confetti` (`^6.1.0`) — Displays celebratory confetti when `gameWon` is true.

## Getting Started

1. Install dependencies:
   ```bash
   npm install
