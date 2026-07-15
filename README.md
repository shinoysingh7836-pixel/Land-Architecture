# Lands Digital Architecture Atlas

An interactive map of the Forestry & Parks / Lands Division digital ecosystem —
11 system ecosystems, 66 systems and 107 data flows unified into one scene,
rebuilt from the 12 Visio (.vsd) ecosystem diagrams. Shared hubs (GENESIS, GLIMPS,
EDS, DIDS+, ECM, Amazon S3, AER One Stop) appear once and connect across every
ecosystem, stitching the previously separate diagrams together.

## 2D and 3D
Use the 3D / 2D switch in the bottom dock. 3D is an orbitable spatial view;
2D flattens the whole scene into a clean top-down architecture diagram. The
switch morphs smoothly between the two — same data, two ways to read it.

## Icons
Each system is drawn as a professional icon tile keyed to what it is: database,
object-storage bucket, cloud service, service/API, server/infrastructure,
security shield, regulator/government, ETL/process, data warehouse, document
store, external connector, and finance. Colour encodes the layer (see the Layers
legend). These are generic cloud-infrastructure icons, not the branded AWS/Azure
logos — safer for a public Protected A repo. Swap in a licensed icon set anytime.

## Controls
- 3D: drag to orbit, scroll to zoom, right-drag (or shift-drag) to pan
- 2D: drag to pan, scroll to zoom
- Touch: one finger orbit/pan, pinch to zoom, two fingers pan
- Click a node to inspect it and trace its data flows
- Search (top right) jumps to any system
- Layers panel toggles system types on/off
- Dock: 3D/2D, data flow, labels, insights, reset

## Insight cards
Floating cards flag things worth acting on: the GLIMPS status-code fix
(5 = Active/Disposed, 7 = Cancelled), the Land Standing Report legal/revenue
risk, the DIDS+ future-state consolidation, the ALIS decommission dependency,
and the shared AER/DRAS FNC interface.

## Hosting on GitHub Pages
Single self-contained file — no build step.
1. Commit `index.html` (root, or a `/docs` folder). The file must be named exactly `index.html`.
2. Settings → Pages → Deploy from a branch → `main` / `/root` (or `/docs`) → Save.
3. Wait for the green "Your site is live at…" banner, then open the URL.

Three.js loads from a CDN (cdnjs), so viewers need internet. Everything else —
data, icons, layout, styling — is baked into `index.html`.

## Updating the data
The graph lives in the `MODEL` constant near the top of the script:
`systems`, `links`, `annotations`, `dmarkers`. Per-system icons are set in
`ICON_OVERRIDE` (falls back to a per-category default).
