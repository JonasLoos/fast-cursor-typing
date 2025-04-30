# Fast Cursor Typer

[![](TODO)](jonasloos.github.io/fast-cursor-typing/)

A simple web-based application that allows you to type text using directional mouse gestures. Move the mouse in a sequence of three directions (up, down, left, or right) relative to a starting point to select and type a character.

## How it Works

1.  **Start Typing**: Click the central crosshair button. This will attempt to lock the mouse pointer (for better tracking) or activate a "soft capture" mode if pointer lock isn't available/granted.
2.  **Select Character**: Make three consecutive mouse movements away from the center, exceeding the configured sensitivity threshold in one of the four cardinal directions (Up, Down, Left, Right).
    *   Each move narrows down the possible characters, shown on the corresponding directional buttons.
    *   After three moves, the selected character is appended to the output text area.
3.  **Stop Typing**: Click press the `Escape` key. This releases the pointer lock/soft capture and stops registering mouse movements for typing.

## Features

*   **Gesture-Based Typing**: Input text using sequences of mouse movements.
*   **Pointer Lock**: Utilizes the Browser Pointer Lock API for accurate movement tracking when available. Falls back to a less precise "soft capture" mode otherwise.
*   **Configurable Character Set**: Define the exact set of characters available for typing via the "Options" section. The system requires 4<sup>3</sup> = 64 characters; if fewer are provided, the remaining slots are padded with spaces.
*   **Adjustable Sensitivity**: Control how far the mouse needs to move in a direction to register a step via the "Sensitivity" slider in the "Options" section.
*   **Output Management**: Easily copy the typed text to the clipboard or clear the output area.
*   **Pure Client-Side**: Runs entirely in the browser using HTML, CSS, and JavaScript. No server-side component or external dependencies are needed.

## How to Use

1.  [Click here]( jonasloos.github.io/fast-cursor-typing/)
2.  Click the central button to begin.
3.  Perform sequences of three directional mouse movements to type characters.
4.  Click outside the button or press `Esc` to finish.
5.  Expand the "Options" section to customize the character set and sensitivity.
6.  Use the "Copy" and "Clear" buttons below the output as needed.
