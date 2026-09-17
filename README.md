# The Eye of the Argument

A zero-build manuscript reading room in the TitanicParker publication format.

## Repository structure

This repository is intentionally prepared as a two-file receptacle until the manuscript arrives:

```text
/
├── index.html
└── README.md
```

When the manuscript is ready, add:

```text
manuscript.md
```

The finished publication unit is therefore:

```text
/
├── index.html
├── manuscript.md
└── README.md
```

## Manuscript workflow

`index.html` always loads the manuscript by relative path:

```js
./manuscript.md
```

No edit to `index.html` is required when the manuscript is added or replaced.

The preferred Markdown structure is:

```md
# The Eye of the Argument

## Major section

Normal prose paragraph.

### Subheading

More prose.
```

The first `#` heading becomes the visible title and browser title automatically.

## Reader behaviour

The reader includes:

- runtime Markdown rendering
- DOM sanitisation
- browser-native text-to-speech
- Pakistani English preference when available
- 1.05× default narration speed
- speed and voice controls
- click-to-listen from the manuscript
- current-block highlighting
- karaoke-style current-word tracking beneath the active text
- reading/listening progress saved locally
- resume from the reader's last place
- responsive layout
- dark mode
- print styling

## Hosting

The site is static. It requires no package installation, build step, framework, server, or database.

When published through GitHub Pages, serve from the repository root on `main`.
