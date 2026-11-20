# Jorge Villalobos — personal portfolio

A bilingual, responsive portfolio built with semantic HTML and shared CSS. No JavaScript, external fonts, dependencies, or build step.

- `index.html`: English homepage (`/`).
- `es/index.html`: Spanish homepage (`/es/`).
- `assets/styles.css`: shared layout, typography, and responsive styles.
- `assets/favicon.svg`: local initials favicon.

## Local preview

From the repository root, run:

```sh
python3 -m http.server 8000
```

Open http://localhost:8000/ and http://localhost:8000/es/. Stop the server with Ctrl+C.

Before release, check both languages at mobile, tablet, and desktop widths; navigate with Tab; test the skip link and language navigation; and check zoom at 200%.

## GitHub Pages deployment

When publication is approved, commit and push the files to the intended publishing branch. In the repository's **Settings → Pages**, select **Deploy from a branch**, choose that branch and **/ (root)**, and save. For the `jovillal.github.io` repository, GitHub Pages serves the English homepage at https://jovillal.github.io/ and Spanish at https://jovillal.github.io/es/.

No build command is required. Relative asset and language links also support a subdirectory preview. This iteration has not been published by the implementation process.

## Content maintenance

Edit the two HTML pages together to keep translations aligned. Project results reflect the supplied brief. The API case study is anonymous; Education Manager is explicitly a prototype. Contact uses only the approved public GitHub profile. No email, LinkedIn URL, private project links, analytics, or contact form is included.

## Future contact links

Both pages use a labeled `.contact-links` navigation group that wraps on narrow screens. Add approved LinkedIn and email links and a local downloadable CV to this group in both languages when the actual URLs, address, and CV are approved for publication. Use meaningful translated link labels and the `download` attribute for the local CV. Until then, only the approved GitHub link is rendered; there are no placeholder links or unpublished contact details in the HTML.
