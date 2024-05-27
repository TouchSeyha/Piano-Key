# Piano Player Web Application

This repository contains the code for a simple web-based piano player application.

## HTML Structure

The HTML file (`index.html`) is structured as follows:

### Title

- The webpage title is set to "Piano Keys".

### Body Content

1. **Title and Instructions**:
   - `<p class='title'>Piano Player</p>`: A title for the application.
   - `<p id='demo'>Follow the song below to play the piano.</p>`: Instructions for the user.

2. **Piano Keys**:
   - A section with the class `piano` containing individual `section` elements for each key.
   - Each key is identified by an ID (`c-key`, `c-sharp-key`, etc.) and class (`key` for white keys, `black-key` for black keys).
   - Each key contains a child `section` with the note name.

3. **Lyrics and Notes**:
   - A section with the ID `lyrics` containing individual columns for each word and corresponding note of the song "Happy Birthday".
   - Each column has a word (`section` with ID `word-one`, etc.) and a note (`section` with ID `letter-note-one`, etc.).

4. **Navigation Buttons**:
   - Four buttons to navigate through the lines of the song and to reset the lyrics display.

### Script

- The HTML file includes a link to an external JavaScript file (`main.js`), which will handle the interactive functionality of the piano keys and buttons.

## CSS Styles

The CSS file (`style.css`) includes styles for the entire webpage:

### Global Styles

- `body`: Sets margin and padding to 0, uses sans-serif font, and sets background color to `#ffc63f`.

### Title and Description

- `.title`: Styles the title with font size, margins, color, uppercase text, letter spacing, and center alignment.
- `#demo`: Styles the description with center alignment, font size, margin, color, letter spacing, and italic style.

### Piano Keys

- `.piano`: Sets the dimensions, display, margin, and background color for the piano container.
- `.key`: Styles white keys with dimensions, display, border, shadow, background color, and text color.
- `.black-key`: Styles black keys with dimensions, display, background color, text color, positioning, and padding.
- `.keynote`: Styles the note labels on white keys with dimensions, alignment, margins, and color.
- `.black-keynote`: Styles the note labels on black keys similarly to `.keynote`.

### Lyrics and Notes

- `#lyrics`: Sets dimensions, display, margin, padding, and background color for the lyrics section.
- `#column-one`, `#column-two`, etc.: Styles the columns with dimensions, display, alignment, and margin.
- `#column-optional`: Initially hidden.
- `#word-one`, `#word-two`, etc.: Styles the word elements with background color, dimensions, padding, letter spacing, and text color.
- `#letter-note-one`, `#letter-note-two`, etc.: Styles the note elements with color, dimensions, and margins.

### Buttons

- `#first-next-line`, `#second-next-line`, etc.: Styles the navigation buttons with dimensions, font size, positioning, margins, border, background color, text color, letter spacing, and cursor.

## JavaScript Functionality

The JavaScript file (`main.js`) includes:

### Variables

- `keys`: An array storing the IDs of piano keys.
- `notes`: An array storing the DOM elements of the piano keys.
- `nextOne`, `nextTwo`, `nextThree`, `startOver`: Variables storing the navigation buttons.
- `lastLyric`: Variable storing the '-END' lyric element.

### Functions

- `keyPlay(event)`: Changes the background color of the key to cyan on mouse down.
- `keyReturn(event)`: Reverts the background color of the key on mouse up.
- `eventAssignment(note)`: Assigns `onmousedown` and `onmouseup` event handlers to each note.

### Event Handling

- `notes.forEach(eventAssignment)`: Assigns the event handlers to each key.
- Anonymous functions for `nextOne`, `nextTwo`, `nextThree`, and `startOver` to handle navigation through lyrics and reset functionality.

## How to Use

1. Open the `index.html` file in a web browser.
2. Follow the instructions to play the piano by clicking the keys.
3. Use the buttons to navigate through the lines of the "Happy Birthday" song.

## Files

- `index.html`: The main HTML file containing the structure of the web application.
- `style.css`: The CSS file for styling the application.
- `main.js`: The JavaScript file for adding interactivity to the application.
