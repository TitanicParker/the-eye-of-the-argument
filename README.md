# The Eye of the Argument

A zero-build manuscript reading room in the TitanicParker publication format.

## Repository structure

The publication unit is:

```text
/
├── index.html
├── manuscript.md
└── README.md
```

`manuscript.md` is now live and is the source content for the reading room.

## Manuscript workflow

`index.html` always loads the manuscript by relative path:

```js
./manuscript.md
```

To revise the publication, replace or edit `manuscript.md`. No edit to `index.html` is required for ordinary manuscript changes.

The preferred Markdown structure is:

```md
# Book Title

## Major section

Normal prose paragraph.

### Subheading

More prose.
```

The first `#` heading becomes the visible title and browser title automatically. The current manuscript begins with `# What Happened to the Feet`, so that is the live reading-room title.

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

## Naming convention

The manuscript filename must remain exactly:

```text
manuscript.md
```

Use lowercase `m`. GitHub Pages paths are case-sensitive, and the reader intentionally loads `./manuscript.md`.

## Museum

The museum reading room is:

```text
https://titanicparker.github.io/the-eye-of-the-argument/
```

The museum wrapper loads this repository's `index.html`, which in turn loads this repository's `manuscript.md`.

## Hosting

The site is static. It requires no package installation, build step, framework, server, or database.

When published through GitHub Pages, serve from the repository root on `main`.
