# Map Marker Studio

A lightweight browser-based U.S. map editor for creating, editing, searching, and sharing reusable pins. It began as a way for remote coworkers to see how geographically distributed the group was, and is now generalized for meetups, communities, trips, field work, service areas, and other shared places.

## Open it

1. Clone this repository or unzip its **Code → Download ZIP** archive.
2. Open `index.html` in the repository's root folder in a modern browser.
3. Add pins individually or import a CSV. The map updates while you edit.

CSV columns must be named `name`, `location`, and optionally `team`. Locations can be a five-digit ZIP code, city and state, or a full state name. See `sample-pins.csv` for an example.

The checkout is the runnable package: there is no build step, package installation, or `dist/` directory. Keep the root HTML, CSS, JavaScript, and `vendor/` files together when copying the editor or viewer to another folder or a static web host. The screenshots are documentation, not runtime dependencies.

The editor stores its draft in that browser. Use **Backup data** before moving computers or clearing browser data.

## View and save

- `index.html` is the editable version with a live map.
- `viewer.html` is the included view-only version.
- Both pages load `map-data.js`. Use **Save shared data**, then replace that file with the downloaded copy to publish the editor's current records to both pages.
- **Create view-only map** downloads one self-contained `map-marker-studio-view-only.html` file containing the current pins. It can be opened or shared without the rest of the folder.

The map and map software are included in the download. Viewing saved markers works offline and does not require an account, API key, or paid service. An internet connection is needed only when converting a new ZIP code or city/state into map coordinates. Full-state locations work offline.

State boundaries are derived from the U.S. Census Bureau's 2025 cartographic boundary files. Alaska and Hawaii use separate inset maps so they cannot overlap the continental states.

This version supports far more than 50 displayed markers. The generated view-only map is interactive, searchable, and does not expose editing controls.

## Source reuse terms

No project-wide reuse license has been selected for Map Marker Studio's original source. Public availability does not supply a permissive reuse grant; contact the maintainer before reusing or redistributing that source. A future license choice remains an owner decision.

Bundled Leaflet retains its own [license and copyright notices](vendor/LICENSE-LEAFLET.txt). State-boundary attribution is described above; it is separate from the original application source.
