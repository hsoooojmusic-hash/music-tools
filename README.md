# Woodshed

Free browser tools for guitar practice.

| Tool | What it's for |
|---|---|
| **Root to Root** | Travel between numbered stops on the neck inside a scale, arpeggio or interval |
| **Fret Roulette** | Random fret positions as a starting note for finding melodies by ear |
| **Blind Voicings** | Name a chord shape from its notes, then see why it's called that |
| **Spelled Out** | Drills for letter steps, intervals up and down, and chord spelling |
| **Interval Mirror** | Every interval above and below a root, spelled correctly |

Everything is plain HTML, CSS and JavaScript with no build step. Settings and scores are saved in each visitor's browser.

## Folder layout

```
index.html              home page
assets/site.css         shared nav bar and base styles
assets/icon.svg         site icon
root-to-root/index.html
fret-roulette/index.html
blind-voicings/index.html
spelled-out/index.html
interval-mirror/index.html
.nojekyll               tells GitHub Pages to serve the files as they are
```

## Publish on GitHub Pages (free)

1. Sign in at github.com and create a new repository (the **+** menu, then **New repository**). Name it something like `woodshed` and set it to **Public**.
2. On the new repo's page, click **uploading an existing file**. Drag in everything from this folder, keeping the folders. Then click **Commit changes**.
   - `.nojekyll` is a hidden file, so your file browser may not show it. The site works without it.
3. Open **Settings → Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose the **main** branch and the **/ (root)** folder, then click **Save**.
4. Wait a minute or two, then refresh that page. It shows your site's address, usually `https://YOUR-USERNAME.github.io/woodshed/`.

To update a tool later, upload the new version of its `index.html` into the same folder. The site redeploys on its own.

## Adding another tool

1. Make a new folder, for example `my-tool/`, and put the tool's page in it as `index.html`.
2. Copy the `<nav class="ws-nav">…</nav>` block and the small script after it from any tool page into the top of the new page's `<body>`. Add `<link rel="stylesheet" href="../assets/site.css">` to its `<head>`.
3. Add a link to the new tool in the nav block on every page, and add a card for it to the home page `index.html`.
