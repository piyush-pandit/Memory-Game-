# Product Requirements Document: Hangman

## Overview

Add a standalone Hangman word-guessing game to this repository. Like the Memory Game, it should run directly in a modern browser from a single HTML file, with no build step, external libraries, network access, or server-side components.

## Goal

Offer a simple, accessible word-guessing game for casual play on desktop and mobile while keeping the existing Memory Game unchanged.

## Users and user stories

- As a player, I can start a round with a randomly selected word and category.
- As a player, I can guess letters using either an on-screen keyboard or my physical keyboard.
- As a player, I can see correct guesses in the word, incorrect guesses in the drawing, and how many mistakes remain.
- As a player, I can tell when I win or lose, see the answer after a loss, and start another round.
- As a player, I can play on a small screen and navigate controls using a keyboard or assistive technology.

## Scope

### In scope

- One-player Hangman with a built-in, curated word list and category labels.
- A new random word each round, avoiding an immediate repeat when possible.
- A six-mistake limit with a progressively drawn, clearly recognizable figure.
- On-screen A-Z letter buttons and physical keyboard letter input.
- Visible feedback for guessed, correct, and incorrect letters.
- Win/loss messages, answer reveal on loss, and a new-round control.
- Responsive layout, semantic controls, visible focus, and live status announcements.
- Optional light/dark appearance toggle for the current page session.
- Single-file HTML, CSS, and JavaScript implementation with no external dependencies.

### Out of scope

- Multiplayer, accounts, online word services, or downloadable assets.
- Timed rounds, hints, difficulty settings, or persistent scores.
- Changes to Memory Game rules or behavior.

## Functional requirements

1. On load, initialize a playable round with a random word and its category.
2. Display one blank per word letter; spaces in multiword answers remain visible and do not require guesses.
3. Accept only A-Z guesses. Ignore non-letter keyboard input and repeated guesses without consuming an attempt.
4. A correct guess reveals all matching occurrences. An incorrect guess adds one body part and reduces remaining attempts.
5. The round ends immediately when every letter is revealed or the six-mistake limit is reached.
6. On a win, show a success message. On a loss, show the answer. Disable further guesses until a new round starts.
7. Starting a new round resets guesses, drawing, status, and controls.
8. The appearance toggle changes the page palette without resetting or affecting the active round.
9. Game state is in memory only; reloading starts a new round.

## Non-functional requirements

- Open and play directly as a local HTML file in current desktop and mobile browsers.
- Do not load remote resources or introduce package/build requirements.
- Keep text, buttons, and game state readable in both appearance modes.
- Ensure all actions are keyboard-operable and focus indicators remain visible.
- Announce game status changes using an accessible live region.
- Preserve the existing Memory Game and its files' behavior.

## Acceptance criteria

- Opening `hangman.html` starts a valid round without network access.
- Both the on-screen keyboard and physical A-Z keys make guesses.
- Repeated guesses do not change attempts or duplicate feedback.
- Correct letters reveal every occurrence; incorrect guesses draw in sequence.
- A player can win before six mistakes, or lose on the sixth; both outcomes prevent extra guesses.
- A loss reveals the answer, and the new-round button starts a clean round.
- The theme control changes the appearance without changing round state.
- The layout and controls remain usable on desktop and narrow mobile screens.
- The existing `memory-game.html` remains unchanged by the Hangman implementation.

## Definition of done

The standalone game meets the acceptance criteria, its JavaScript parses, it loads locally in a browser, and the repository README explains how to launch it.
