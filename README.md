Initial release of Flip and Burn orbital planner
Single-file web app: a live solar system map with time controls and a
torch-ship route planner. No build step or dependencies; open
index.html or serve it with GitHub Pages.

Map
- Planets from JPL approximate Keplerian elements (Standish, valid
  1800-2050); Ceres, Vesta, Pallas, Hygiea and Eros from JPL osculating
  elements, propagated two-body
- Major moons with real radii and periods (notional phase except Luna)
- Date jump, variable playback speed, reverse time, pan/pinch/zoom
- sqrt(r) compressed or true-scale display

Route planner
- Flip & burn: constant thrust, midpoint flip, velocity-matched arrival
- Burn-coast-burn: fastest trip within a delta-v budget
- Hohmann: patched-conic transfer with launch-window search
- Live mode re-solves the route continuously as time plays
- Departure-date scan chart showing launch windows
- Trip playback with the ship oriented along its thrust vector

Custom objects
- Circular orbiters around any body, period derived from GM
- Lagrange points L1-L5 for any body and its primary; collinear
  points solved exactly from the mass ratio, stability flagged
- Stored in browser localStorage, with JSON export/import

Known limits: torch routes ignore gravity (fine at torch thrust, warned
below 0.05 g); Hohmann assumes circular, coplanar orbits.

Unofficial fan project. Released under the Unlicense.
