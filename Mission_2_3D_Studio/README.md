# Venture 3D Studio — Mission 2

Standalone browser studio for the Oasis live translation earbuds concept. The app builds an editable procedural Three.js model, rather than claiming to reconstruct geometry from the reference image. The provided concept image is included as a persistent reference.

## Open it

Serve this folder from a local static web server, then open its URL in a modern browser. The 3D engine and export helpers load from jsDelivr, so the first load needs internet access. No API key is used. The app uses browser ES modules and may not work when opened directly as a `file://` URL.

## Student guide

1. Orbit with a mouse drag and zoom with the wheel. Use Front, Side, and Top to inspect; Reset view returns to the studio angle.
2. Choose a component in Scene Objects.
3. Adjust scale, rotation, color, metallic appearance, and roughness in the inspector.
4. Upload an image to keep another reference visible. It remains a reference, not a texture or 3D reconstruction.
5. Save project downloads `Oasis_editable_project.json`; import a compatible backup with Import project backup.
6. Confirm model checks that the scene can export a binary GLB and downloads `Venture_3D_Confirmed_Handoff.zip`. The ZIP contains `model.glb`, `model-manifest.json`, `project.json`, `preview.png`, and `README.txt`.

The model is a stylized editable interpretation of the concept, not an automatic image-to-3D reconstruction. Dimensions are relative model units; it does not include the reference's veined marble texture or mechanically accurate internals.

## Deploy

This project uses relative `./` asset paths for GitHub Pages subpaths. Enable Pages for the repository and serve `Mission_2_3D_Studio/` as the site root, or publish the folder through a workflow that copies its contents to the Pages artifact.

## Current limits

The initial build includes earbuds, bottle, and gift box templates. Project backups preserve transforms and colors but do not embed uploaded image bytes or arbitrary mesh geometry. GLB and ZIP packaging run in the browser.