# Portfolio site

WIP! static site

AI notes:

## Adding a live WebGL/WebAssembly demo

If you compile a project with Emscripten, drop the output files (`.html`/`.js`/`.wasm`)
into that project's folder (e.g. `/projects/fluid-sim/demo/`) and either link to the
compiled `.html` directly, or embed it with an `<iframe src="demo/index.html">` inside
the `.media` block.

## Hosting on GitHub Pages

1. Push this whole folder to a repo named `yourusername.github.io` (or any repo,
   then enable Pages on it).
2. Settings → Pages → set source to the `main` branch, root folder.
3. Site goes live at `https://yourusername.github.io/`.

Because every page lives in its own folder with an `index.html`, links like
`projects/terrain-shader/` resolve automatically without needing `.html` in the URL.
