# Lands Digital Architecture Atlas

An interactive 3D map of the Forestry & Parks / Lands Division digital ecosystem —
11 system ecosystems, 66 systems and 107 data flows unified into one navigable scene.
Rebuilt from the 12 Visio (.vsd) ecosystem diagrams so shared hubs (GENESIS, GLIMPS,
EDS, DIDS+, ECM, Amazon S3, AER One Stop) appear once and connect across every district,
stitching the previously separate diagrams together.

## Controls
- Drag to orbit, scroll to zoom, right-drag (or shift-drag) to pan
- Touch: one finger orbit, pinch to zoom, two fingers pan
- Click a node to inspect it and trace its data flows
- Search box (top right) to jump to any system
- Left panel toggles system layers on/off
- Bottom dock: data flow, labels, insights, reset view

## Insight cards
Floating cards flag things worth acting on: the GLIMPS status-code fix
(5 = Active/Disposed, 7 = Cancelled), the Land Standing Report legal/revenue risk,
the DIDS+ future-state consolidation, the ALIS decommission dependency, and the
shared AER/DRAS FNC interface.

## Hosting on GitHub Pages
This is a single self-contained file — no build step.
1. Commit `index.html` to your repo (root, or a `/docs` folder).
2. Repo Settings → Pages → deploy from branch → pick `main` and `/root` (or `/docs`).
3. Open the published URL.

Three.js loads from a CDN (cdnjs), so the page needs internet access when viewed.
Everything else — data, layout, styling — is baked into `index.html`.

## Updating the data
The architecture graph lives in the `MODEL` constant near the top of the
second `<script>` block: `systems`, `links`, `annotations` and `dmarkers`.
Edit those arrays to add a system, a flow, or an insight card.
