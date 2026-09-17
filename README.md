# Perihelion

Front page for a fictional AI stock-trading service. Live at
**https://dittonjs.github.io/cool-designs/**

Single self-contained `index.html` — no build step, no dependencies beyond two
Google Fonts.

## The idea

*Perihelion* is the point in an orbit closest to the sun: closest approach,
precise timing.

The hero is a **price chart drawn in polar coordinates**. One full revolution is
twelve months, and distance from the centre is cumulative return, so each ring
is 10%. Three assets spiral outward from a central star and the Perihelion line
ends much further out than the S&P 500 or the Nasdaq. The orbital metaphor and
the performance data are the same object, which is why the page needs so few
words to make its claim.

Returns are seeded random walks, de-trended so each one lands exactly on its
stated figure — the page is a design piece, and it says "Simulated results" on
its face.

## Notes

- **Colour** carries the argument: the AI is warm (sodium amber), the market is
  cold (pale ice blue). No red/green anywhere.
- **Type** is one family, Archivo variable, set wide (`wdth 118`) for the
  headline. IBM Plex Mono appears only inside the chart, for telemetry.
- **Motion** is one orchestrated page-load sequence: starfield, then the star
  blooms, then the spirals draw outward, then the headline wipes up from a mask,
  then the labels resolve. After that the field rotates at 0.34°/s — roughly one
  turn every 17 minutes. `prefers-reduced-motion` renders the final state
  immediately and never rotates.
- Rendering pauses on `visibilitychange` and resumes on the same timeline.
