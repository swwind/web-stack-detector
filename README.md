# Web Stack Detector

A Firefox and Chrome extension that works out what the page you are looking at
was built with — the framework, the UI library and the bundler — and turns the
toolbar icon into that project's logo.

Available on the official stores:

- [Chrome Web Store](https://chromewebstore.google.com/detail/web-stack-detector/jagakebomapmaajkbbldhbilhgedlkmp)
- [Firefox Add-ons](https://addons.mozilla.org/en-US/firefox/addon/web-stack-detector/)

<details>
<summary>Screenshots</summary>

![example](example.png)

</details>

## Features

Currently supports the following technologies.

### Meta-framework

| Name | Version range |
| --- | --- |
| Next.js | Exact version |
| Fresh | ≤ 1 or ≥ 2 |
| Nuxt | — |
| SvelteKit | — |
| Astro | Exact version |
| Gatsby | Exact version |
| Docusaurus | Exact version |
| VitePress | Exact version |
| Rspress | Exact version |
| Remix | Exact version (3.x) |

### UI library

| Name | Version range |
| --- | --- |
| React | Major version |
| Preact | — |
| Vue | 2 / 3 |
| Angular | Exact version |
| AngularJS | Exact version |
| Svelte | Major version |
| Solid | — |
| Qwik | Exact version |
| Lit | Exact version |
| Alpine.js | Exact version |
| htmx | Exact version |
| jQuery | Exact version |
| Stimulus | — |
| Ember.js | — |
| Backbone.js | Exact version |
| Knockout | Exact version |

### Bundler

| Name | Version range |
| --- | --- |
| Vite | Major version range |
| webpack | Major version |
| Rspack | 1.x exact / ≥ 2 |
| Turbopack | — |
| Parcel | Major version |
| esbuild | — |
| Rollup | — |

## Build

Needs Node 20+. The build copies files, picks the right manifest and downscales
the toolbar icons, which is the one thing that needs a dependency (sharp).

```sh
git clone https://github.com/swwind/web-stack-detector.git
cd web-stack-detector
npm install
npm run build
```

That writes two loadable folders:

```
dist/chrome     manifest with a service-worker background
dist/firefox    manifest with an event-page background + a gecko id
```

They share every line of code and differ only in the manifest.

## License

MIT, for the code — see [LICENSE](LICENSE). The icons are a separate matter;
see the credits below.

## Icon credits

Most icons are the projects' own artwork:

| Icon | Source |
| --- | --- |
| vite, webpack, parcel, rollup, esbuild, react, vue, angular, svelte, next, nuxt, gatsby, ember, qwik, remix | [material-icon-theme](https://github.com/material-extensions/vscode-material-icon-theme) (MIT) |
| solid, lit, preact, docusaurus, vitepress, stimulus | the project's own published SVG — solidjs.com, lit.dev (the `flame` symbol out of its full lockup), the preactjs.com branding assets, docusaurus.io, vitepress.dev, stimulus.hotwired.dev |
| jquery, alpine, htmx, angularjs, backbone | [devicon](https://github.com/devicons/devicon) (MIT) — those five publish a wide wordmark as their own asset, and devicon carries the square symbol from the same logo |
| rspack | the site favicon, `https://assets.rspack.rs/rspack/favicon-128x128.png` |
| turbopack | the Turbo mark from the [vercel/turborepo](https://github.com/vercel/turborepo) README |
| astro | the mark from `https://astro.build/favicon.svg` |
| fresh | the [official Fresh SVG](https://github.com/freshframework/fresh/blob/main/www/static/logo.svg) |
| knockout | the [Knockout organisation](https://github.com/knockout) avatar on GitHub — the same script K as their favicon, at 460 px instead of 16 |
| sveltekit | the Svelte mark, which is SvelteKit's own branding too — the toolbar cannot tell the two apart, the popup can |

These icons are their respective projects' trademarks. Check the applicable
licence and trademark terms before redistribution.
