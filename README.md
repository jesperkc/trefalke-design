# @trefalke/design

The one place Trefalke's look is decided. Two apps consume it:

- trefalke.com (`jesperkc/trefalke.com`)
- the bag builder (`jesperkc/bike-frame-bag-configurator`), served at `/bags/builder/`

| File | What it is |
| --- | --- |
| `tokens.css` | Palette, type families, easing curves, as CSS custom properties. |
| `fonts.css` | The `@font-face` rules. Urls are relative, so the app's bundler hashes them. |
| `fonts/` | The woff2 files. |
| `index.css` | Imports both of the above. |
| `DESIGN.md` | The design system document. Agents in either repo read this one. |

## Using it

```css
@import '@trefalke/design/index.css';
```

Vite resolves the import, bundles the fonts and applies the app's `base`.
To preload a font: `import url from '@trefalke/design/fonts/barlow_semicondensed_400.woff2?url'`.

## Changing the design

1. Edit the file here, commit, bump `version` in `package.json`, tag it (`git tag v0.2.0 && git push --tags`).
2. In each app: `npm run design:update`, then commit `package.json` and `package-lock.json` and deploy.

Apps pin a tag, so a change here never reaches a site until that site updates.
Neither app may redeclare a value that lives here; alias it instead.
