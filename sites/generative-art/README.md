# Flow Field

A generative art sketch built with p5.js. Hundreds of particles drift across a dark canvas, steered by an invisible vector field generated from Perlin noise. The result looks like flowing silk or slow-moving smoke.

## How to run

Open `index.html` directly in a browser — no build step needed.

## Controls

- **Click / drag** — spawn a burst of particles at your cursor
- **Change Palette** — cycle through 6 color palettes (Aurora, Ember, Ocean, Forest, Candy, Monochrome)
- **Reset** — clear the canvas and restart
- **Save Image** — download the current frame as a PNG

## How it works

Each particle samples a [Perlin noise](https://en.wikipedia.org/wiki/Perlin_noise) field at its current position to get an angle, then steers toward that angle. Because noise is smooth and continuous, nearby particles flow together in organic-looking streams. The noise field slowly shifts over time (`zOffset`), keeping the animation alive.
