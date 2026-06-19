# models/

**`heart.glb` is already here** — "Human Heart Beating - Annotations" by dcpisith,
a fully rigged anatomical heart with skeletal animation sourced from Sketchfab.
It is licensed **CC BY 4.0**, so attribution is required: see
`ATTRIBUTION.txt` (copy that into Appendix D of the report).

`index.html` already loads it. If you want to swap in a different model, follow
the steps below.

## Where to get other models
- **NIH 3D** — https://3d.nih.gov — open portal; models are under a Creative
  Commons licence or released to the public domain, and you can export GLB
  directly from the in-browser viewer. Good first stop for anatomy.
- **Sketchfab** — filter Downloadable + Creative Commons; several heart models
  are CC-BY and marked as suitable for AR/VR and education. CC-BY means you
  **must credit the author**.
- **BodyParts3D / Anatomography** (DBCLS) — anatomy parts; check the stated
  licence (typically CC-BY-SA) before use.

Avoid "free" marketplace models whose licence is "royalty-free" or
"editorial only" — those are not open licences and are not safe for a
submitted academic deliverable.

## Wire it up (in index.html)
1. Add an assets block inside `<a-scene>`:
   ```html
   <a-assets>
     <a-asset-item id="heartModel" src="models/heart.glb"></a-asset-item>
   </a-assets>
   ```
2. Replace the primitive cluster inside the `#heart` entity with:
   ```html
   <a-entity gltf-model="#heartModel" position="0 0 0" rotation="0 0 0"
             scale="0.01 0.01 0.01"></a-entity>
   ```
   Tune `scale` on this inner entity (models are often in millimetres). Leave
   the `#heartScale` wrapper and the `#heart` beat animation alone so the
   heartbeat keeps working.
3. If the GLB is Draco-compressed, point A-Frame at the decoder on `<a-scene>`:
   ```html
   <a-scene gltf-model="dracoDecoderPath: https://www.gstatic.com/draco/versioned/decoders/1.5.6/">
   ```
4. If the model has its **own** beating animation, load `aframe-extras` and add
   `animation-mixer` to the model entity instead of using the scale pulse.

## For Appendix D, record:
| Field | Example |
|-------|---------|
| Model name | Human Heart |
| Author | (creator handle) |
| Source URL | https://3d.nih.gov/... |
| Licence | CC0 / CC-BY 4.0 / public domain |
| Attribution shown | yes/no, where |
