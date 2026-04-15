# Awesome-Checkboxes-and-Radios

Small library for customizing checkboxes and radios built in sass and using Material Symbols icons as source, can be extended to other icon sources.

## Local preview

The Dev Container now installs the preview dependency automatically and starts the local server on boot.

Open the forwarded port `3000`, or run the preview manually with:

```bash
npm run dev
```

Then open `http://localhost:3000`.

## CSS build

For this repo, the most efficient workflow is to keep `style.scss` as the source of truth and let Dart Sass watch it:

```bash
npm run watch:css
```

Use this for daily development. When you want the distributable files, run:

```bash
npm run build:css
npm run build:css:min
```

That keeps rebuilds incremental and avoids recompiling more than the single source file.

## Classes

- Put `acr`, `acr-fill`, and optionally `acr-{icon}` on the `input`.
- Wrap the `input` in a `label` so the text stays clickable and accessible.
- `acr-fill` draws the frame and checked background, while `acr-md-{icon}` injects the icon glyph from the Material Symbols font.
- The icon itself is rendered with `::before`, `content`, and `font-family` on `input.acr::before`.
- The current map is intentionally small and can be expanded later with other prefixes for other icon sets.
