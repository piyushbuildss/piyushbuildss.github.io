# notes

A plain HTML/CSS personal notes site. No build step, no framework — what's in this folder is exactly what gets served.

## Structure

```
index.html              ← homepage, the list of notes
style.css                ← the one stylesheet, shared by every page
notes/
  example-note/
    index.html            ← one folder per note, each with its own index.html
.nojekyll                 ← tells GitHub Pages not to run its Jekyll processor
```

URL path = file path. `notes/example-note/index.html` becomes `yourname.github.io/notes/example-note/`.

## Before you deploy

1. In `index.html` and every note's `index.html`, replace `YOUR-USERNAME` with your GitHub username, and `you@example.com` with your real email (or delete that link).
2. Delete or rewrite `notes/example-note/` — it's a demo showing how headings, blockquotes, and code blocks render.

## Adding a new note

1. Duplicate `notes/example-note/` and rename the folder, e.g. `notes/india-and-rank-fetish/`.
2. Write inside its `index.html` — it's just HTML inside the `<article>` tag: `<p>`, `<h2>`, `<blockquote>`, `<pre><code>`.
3. Add one `<li class="note-item">…</li>` entry to the list in the root `index.html`, linking to the new folder.

That's the entire workflow. No CMS, no rebuild command.

## Deploying (GitHub Pages)

See the deployment steps given separately — short version: push this folder to a repo named `YOUR-USERNAME.github.io`, turn on Pages in the repo settings, done.
