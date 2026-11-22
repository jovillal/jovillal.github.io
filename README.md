# Jorge Villalobos — personal portfolio

A bilingual, responsive portfolio built with semantic HTML and shared CSS. No JavaScript, external fonts, dependencies, or build step.

- `index.html`: English homepage (`/`).
- `es/index.html`: Spanish homepage (`/es/`).
- `case-studies/api-reliability/index.html`: English API reliability case study.
- `es/casos/confiabilidad-api/index.html`: Spanish API reliability case study.
- `assets/styles.css`: shared layout, typography, and responsive styles.
- `assets/favicon.svg`: local initials favicon.
- `assets/cv/`: approved English and Spanish PDF resumes, linked from the corresponding contact sections.

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

Keep both homepage translations and both case-study translations aligned. Project results reflect the supplied brief. The API case study is anonymous; Education Manager is explicitly a prototype. Contact includes the approved email, LinkedIn, GitHub, and a language-specific CV download. No private project links, analytics, or contact form is included.

## CV downloads

The contact sections use the existing button styling and wrapping `.contact-links` group. English links to `assets/cv/Jorge_Villalobos_CV_Portfolio_EN.pdf`; Spanish links to `../assets/cv/Jorge_Villalobos_CV_Portfolio_ES.pdf`. Relative paths work with both GitHub Pages and the local Python server, including subdirectory previews. The `download` attribute requests a file download.

Keep the approved PDFs unchanged. When replacing them with newly approved versions, retain the filenames and verify both downloads in the local preview. Check the contact sections in both languages at desktop, 375px, and 320px widths.

## API reliability case study

The API Reliability card links to the corresponding case study in each language. Each case study links back to its language’s homepage and directly to its translation. Shared CSS supplies the layout, outcome highlights, responsive behavior, and keyboard focus styles; no build step or JavaScript is needed.

Preview `/case-studies/api-reliability/` and `/es/casos/confiabilidad-api/` as well as both homepages. Verify navigation in both directions, language switching, skip links and visible keyboard focus, and no horizontal overflow at 1440px, 375px, and 320px. Check local asset and fragment links, including from a subdirectory preview.

Keep the company anonymous and distinguish shared team standards from progressively enforced technical controls. Retain the limits on adoption and the approved metrics without deriving an incident-reduction percentage.
