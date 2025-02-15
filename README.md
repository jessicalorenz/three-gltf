# three-gltf
A repo to quickly display any compressed model (gltf format) using Three.js.
- Supports gltf-pack, gltf-pipeline and Blender exports.

### Installation
1. Clone the repo.
2. Run `npm install` to install all the dependencies
3. Use `npm run dev` to compile the project in development mode
4. Use `npm run build` to compile the project in production mode
5. Open `index.html` using Live Server

## Notes
- index.html - Display the GLTF model on the full page.
  - Source files:
    - app.js
    - app.scss
  - Output files: _Generated by Webpack after you compile the project_
    - bundle.js
    - main.css
  - Everything is written as an exportable class named `Sketch` so it can be easily imported using ES6+ syntax.
  - In case your model is compressed with Blender or gltf-pipeline, DRACO compression is applied over the model so make sure you include the `draco-files` folder in your project.
  - In case your model is compressed with gltf-pack, it uses quantisation to compress the model so make sure you correctly import the MeshoptDecoder from three module.
  - All animations are played by default if provided in the GLTF.
  - The model is displayed in MeshNormalMaterial, so in case normals are not provided, the model will be solid black.
