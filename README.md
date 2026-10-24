# Delphine PA Dang: personal website

A [Quarto](https://quarto.org) website you build and edit in RStudio.

## What's in the folder

| File | What it is |
|---|---|
| `delphine-website.Rproj` | Double-click this to open the project in RStudio |
| `_quarto.yml` | Site settings: title, menu, social links, footer |
| `theme.scss` | Colours (pastel green + blue) and font (Inter) |
| `assets/site.html` | The interactive features |
| `index.qmd` | Home page |
| `art-music.qmd` | Art & Music page |
| `research.qmd` | Research page |
| `about.qmd` | About me page |
| `images/` | Posters and any other pictures |
| `docs/` | The finished website (created when you render; don't edit by hand) |

## 1. Open it in RStudio

1. Install [RStudio](https://posit.co/download/rstudio-desktop/) (recent versions already include Quarto). If RStudio says Quarto is missing, install it from <https://quarto.org/docs/get-started/>.
2. Unzip this folder somewhere permanent (e.g. Documents).
3. Double-click **`delphine-website.Rproj`**.

## 2. Preview the site

- Go to the **Build** tab (top-right pane) → **Render Website**. The site opens in the Viewer / your browser.
- Or, in the **Terminal** tab: `quarto preview`. This re-renders every time you save a file.
- Or, from the R console: `install.packages("quarto")` once, then `quarto::quarto_preview()`.

## 3. Edit

- Open any `.qmd` file and type. The text is ordinary Markdown: `**bold**`, `*italic*`, `[link text](https://...)`.
- **Add a film or song:** in `art-music.qmd`, copy one `::: {.work ...}` block from the Film or Music section. For YouTube, set `data-video` to the part of the link after `v=` (it plays in a pop-up). For anything else (Instagram, Vimeo), use `data-link="https://..."` (it opens in a new tab). `data-label` changes the button text.
- **Be My East video:** when it's online, change `::: {.work}` above Be My East to `::: {.work data-video="YOUTUBE_ID"}`.
- **Add a research project:** in `research.qmd`, copy one `::: {.entry ...}` block. `data-when` is the date on the left; add `.open` to show the details from the start.
- **Add an image:** put the file in `images/`, then `![](images/my-photo.jpg){fig-alt="describe the image"}`
- **Interactive parts** (the eye, video pop-ups, survey question, expanding projects) live in `assets/site.html`. You don't need to touch it.
- **Change colours:** edit the hex codes at the top of `theme.scss`.

## 4. Put it online (free)

**Option A: Quarto Pub (easiest).** In the RStudio Terminal run:

```
quarto publish quarto-pub
```

Sign in when the browser opens. Your site will live at `https://<your-username>.quarto.pub/...`.

**Option B: GitHub Pages (nice for a researcher profile).**

1. Create a GitHub repository, e.g. `delphinepadang.github.io`.
2. Upload this whole folder (including `docs/`) to it. GitHub Desktop makes this easy.
3. In the repo: **Settings → Pages → Build from a branch → `main` / `/docs`**.
4. After every edit: Render Website in RStudio, then commit and push again.

**Option C: Netlify Drop.** Render the site, then drag the `docs/` folder onto <https://app.netlify.com/drop>.

Once it's live, add the link to your Linktree and LinkedIn.
