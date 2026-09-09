# Portfolio site

Static site — no build step. Structure:

```
/
├── index.html                     homepage (link list)
├── /assets/
│   ├── css/style.css               shared styles for every page
│   ├── images/                     screenshots, thumbnails
│   └── videos/                     screen captures of demos
└── /projects/
    ├── terrain-shader/index.html   example project page
    └── cornell-box/index.html      example project page
```

## Adding a new project

1. Duplicate `/projects/terrain-shader/` into a new folder, e.g. `/projects/fluid-sim/`.
2. Edit the `<title>`, `<h1>`, meta tags, and body text.
3. Drop a screenshot/video into `/assets/images/` or `/assets/videos/` and reference it
   in the `.media` block (an `<img>` or `<video>` tag instead of the placeholder text).
4. Add a new `<li>` on the homepage (`index.html`) pointing to `projects/fluid-sim/`.

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
