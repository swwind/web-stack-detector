# Web Stack Detector

A Firefox and Chrome extension that identifies the web stack used by the page
you are viewing and changes the toolbar icon to match it.

![The extension popup](example.png)

## Install

- [Install from the Chrome Web Store](https://chromewebstore.google.com/detail/web-stack-detector/jagakebomapmaajkbbldhbilhgedlkmp)
- [Install from Firefox Add-ons](https://addons.mozilla.org/en-US/firefox/addon/web-stack-detector/)

## Build

Requires Node.js 20 or later. The build copies the extension files, selects the
appropriate manifest, and resizes toolbar icons.

```sh
git clone https://github.com/swwind/web-stack-detector.git
cd web-stack-detector
npm install
npm run build
```

The build creates loadable extension folders for Chrome and Firefox under
`dist/`.

## Development

```sh
npm test
npm run build
npm run validate
npm run icons
```

## License

MIT, for the code — see [LICENSE](LICENSE). The icons are a separate matter;
see the credits below.

## Icon credits

Most icons are the projects' own artwork.

| Icon | Source |
| --- | --- |
| vite, webpack, parcel, rollup, esbuild, react, vue, angular, svelte, next, nuxt, gatsby, ember, qwik, remix | [material-icon-theme](https://github.com/material-extensions/vscode-material-icon-theme) (MIT) |
| solid, lit, preact, docusaurus, vitepress, stimulus | The projects' published SVG assets |
| jquery, alpine, htmx, angularjs, backbone | [devicon](https://github.com/devicons/devicon) (MIT) |
| rspack | Rspack site favicon |
| turbopack | The Turbo mark from the [vercel/turborepo](https://github.com/vercel/turborepo) README |
| astro | The mark from [astro.build](https://astro.build/favicon.svg) |
| fresh | The [official Fresh SVG](https://github.com/freshframework/fresh/blob/main/www/static/logo.svg) |
| knockout | The [Knockout GitHub organisation](https://github.com/knockout) avatar |
| sveltekit | The Svelte mark |

These files are the projects' trademarks, whatever the licence on the repository
they were fetched from. Check the applicable terms before redistribution.
