# Miller 3D - 🇮🇹

Interactive 3D visualizer for crystallographic planes defined by Miller indices `(h k l)` inside a cubic unit cell. All in italian.

The application renders the exact intersection between a crystallographic plane and the unit cube `[0,1]³`, including planes with zero or negative Miller indices.

## Features

* Interactive input for Miller indices `h`, `k`, `l`
* Supports positive, negative and zero indices
* Supports barred notation such as `¯1`
* Quick presets:

  * `(1 0 0)`
  * `(1 1 0)`
  * `(1 1 1)`
  * `(3 5 1)`
  * `(-1 1 0)`
* Exact plane–cube intersection
* Automatic handling of equivalent lattice translations for negative indices
* 3D cubic unit cell
* Highlighted vertices and plane boundaries
* Cartesian axes and origin
* OrbitControls for rotation, zoom and pan
* Real-time display of:

  * plane equation
  * axis intercepts
  * resulting polygon geometry
  * number of intersection vertices
  * descriptive interpretation
* Responsive brutalist/minimalist UI
* Single-file application
* No build step required

## Mathematics

For Miller indices

`(h k l)`

the crystallographic plane is represented as

`hx + ky + lz = d`

with intercepts

`x = 1/h`

`y = 1/k`

`z = 1/l`

when the corresponding index is non-zero.

If an index is zero, the plane is parallel to that axis.

For negative Miller indices, an equivalent member of the same crystallographic plane family may be selected through a lattice translation so that the plane can be clearly visualized inside the unit cell.

The infinite plane is intersected with the twelve edges of the unit cube. The resulting intersection points are ordered on the plane and triangulated for rendering.

## Tech Stack

* HTML
* CSS
* JavaScript ES Modules
* Three.js
* OrbitControls

Three.js is loaded directly from a CDN.

No npm installation or bundler is required.

## Run locally

Download or clone the repository and serve the directory with a local HTTP server.

For example with Python:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

You can also deploy it directly using GitHub Pages.

## GitHub Pages

Go to:

`Settings → Pages`

Then select:

`Deploy from a branch`

and choose:

`main / root`

The application will then be available as a static website.

## Example

Try the plane:

`(1 1 1)`

which intersects the cubic unit cell as a triangular section.

Or:

`(-1 1 0)`

which represents a plane parallel to the Z axis with a negative X intercept.

## License

MIT
