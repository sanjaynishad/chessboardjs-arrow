# 🧭 Chessboard.js Arrow Helper

A lightweight utility for drawing arrows on [Chessboard.js](https://chessboardjs.com/) boards. Enhance your visualizations with custom annotations—great for tutorials, analysis tools, and interactive demos.

I originally created this a few years back as a small helper tool, and I'm now sharing it publicly for others who might find it useful.

## Features

- Draw colored arrows between squares
- Easy integration with existing Chessboard.js setups
- Ideal for highlighting moves, strategies, and board states

## Demo

TODO: add demo link

## Installation

Include the script in your HTML file:

```html
<script src="path/to/chessboard-arrow.js"></script>
```

### CSS Note:
Ensure the board container element’s position is set to `relative` to allow arrows to be positioned correctly.

```css
#board-container {
    position: relative;
}
```

## Usage

1. **Initialize the Board Arrow**  
   First, define the configuration options and initialize the board arrow:

```javascript
var configs = {
    width: 15, // default
    fillColor: 'rgba(0, 0, 240, .6)', // default
    headLength: 50 // default
};

// Initialize the board arrow
boardArrow = new ChessboardArrow(boardElOrId, configs);
```

2. **Drawing Arrows**  
   You can now draw arrows on the chessboard based on a move. For example:

```javascript
// Draw an arrow from a move's starting square to its destination
boardArrow.drawArrow(move.from, move.to);
```

3. **Special Arrows with Override Styles**  
   You can also customize the arrow style for specific moves:

```javascript
// Draw an arrow with custom styles
boardArrow.drawArrow(move.to, kingSq, {
    clear: false,  // Don't clear previous arrows
    fillColor: 'rgba(240, 0, 0, .6)'  // Red arrow color
});
```

4. **Clearing Arrows**  
   To clear all arrows from the board:

```javascript
boardArrow.clear();
```

## License

MIT License

---

Feel free to contribute or report issues!
