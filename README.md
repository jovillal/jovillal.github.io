# Jorge Villalobos — personal portfolio

A bilingual, responsive portfolio built with semantic HTML and shared CSS. No JavaScript, external fonts, dependencies, or build step.

- `index.html`: English homepage (`/`).
- `es/index.html`: Spanish homepage (`/es/`).
- `case-studies/api-reliability/index.html`: English API reliability case study.
- `es/casos/confiabilidad-api/index.html`: Spanish API reliability case study.
- `case-studies/education-manager/index.html`: English Education Manager case study.
- `es/casos/education-manager/index.html`: Spanish Education Manager case study.
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

Keep the English and Spanish versions of each homepage and case study aligned. Project results reflect the supplied brief. The API case study is anonymous; Education Manager is explicitly a prototype. Contact includes the approved email, LinkedIn, GitHub, and a language-specific CV download. No private project links, analytics, or contact form is included.

## CV downloads

The contact sections use the existing button styling and wrapping `.contact-links` group. English links to `assets/cv/Jorge_Villalobos_CV_Portfolio_EN.pdf`; Spanish links to `../assets/cv/Jorge_Villalobos_CV_Portfolio_ES.pdf`. Relative paths work with both GitHub Pages and the local Python server, including subdirectory previews. The `download` attribute requests a file download.

Keep the approved PDFs unchanged. When replacing them with newly approved versions, retain the filenames and verify both downloads in the local preview. Check the contact sections in both languages at desktop, 375px, and 320px widths.

## API reliability case study

The API Reliability card links to the corresponding case study in each language. Each case study links back to its language’s homepage and directly to its translation. Shared CSS supplies the layout, outcome highlights, responsive behavior, and keyboard focus styles; no build step or JavaScript is needed.

Preview `/case-studies/api-reliability/` and `/es/casos/confiabilidad-api/` as well as both homepages. Verify navigation in both directions, language switching, skip links and visible keyboard focus, and no horizontal overflow at 1440px, 375px, and 320px. Check local asset and fragment links, including from a subdirectory preview.

Keep the company anonymous and distinguish shared team standards from progressively enforced technical controls. Retain the limits on adoption and the approved metrics without deriving an incident-reduction percentage.

## Education Manager case study

The Education Manager cards link to `/case-studies/education-manager/` and `/es/casos/education-manager/`. Both pages reuse the shared case-study layout and include a responsive HTML/CSS architecture diagram with a textual description of its conceptual relationships. Check both pages and homepage round trips at 1440px, 375px, and 320px, including language switching, diagram readability, skip links, visible focus, and all local links and assets.

Preserve attribution of the initial implementation to the collaborator. Describe retrieval as local and bounded, and keep the prototype’s commercial, productivity, policy-compliance, and operational limitations explicit. Do not add private repository or hosted-demo links, credentials, or infrastructure identifiers.

## Evidence-based visuals

The API Reliability case study includes a localized before/after process figure. Its ordered steps are qualitative: they do not encode time, incident counts, or universal enforcement. The existing narrative and metrics are unchanged.

The Football Probability Model card includes a localized paired-difference plot and the two fixture-pooled log losses. Sources are pinned to public commit `ae063d11a599ac23070a15497c38edebd0859d29` in `jovillal/football-probability-model`:

- [Reviewed development narrative](https://github.com/jovillal/football-probability-model/blob/ae063d11a599ac23070a15497c38edebd0859d29/docs/development-backtest-conditional-dixon-coles-v1.md).
- [Authoritative aggregate report](https://github.com/jovillal/football-probability-model/blob/ae063d11a599ac23070a15497c38edebd0859d29/reports/development-backtest-conditional-dixon-coles-v1.json), version `development-backtest-conditional-dixon-coles-v1` (Git blob `d68b8a7ae750f58164202690e76d95a352a238dc`).

Recorded log loss: uncorrected 180-day exponentially time-weighted Poisson `0.9585391349475223`; conditional Dixon–Coles `0.9608255353548959`. Lower is better. The conditional estimator holds first-stage rates fixed; this is not a claim about every Dixon–Coles model.

The plot uses the report’s mean fixture-wise paired difference (with minus without), `+0.0022864004073735755`, and descriptive two-sided 95% interval `[0.0004920028046178528, 0.004097003049892802]`. The interval is from the recorded operational-week bootstrap: 138 clusters, 10,000 replicates. No experiment or uncertainty estimation was rerun. The symmetric linear axis is `[-0.005, +0.005]`, with zero centered; CSS positions use `50 + value / 0.01 * 100` percent, calculated from full-precision source values. Text displays six decimal places (Spanish uses decimal commas). The line and end caps show the interval; the point shows the paired difference. The same values and interpretation are available as HTML text.

This comparison covers 1,520 fixtures across four development folds within the 2010/11–2018/19 training data. It supports retaining the uncorrected model in development, not official validation, predictive success, or profitability. It does not establish independence or universal ineffectiveness of Dixon–Coles. Keep these boundaries when editing either language.

Both graphics use static HTML/CSS, existing palette tokens, and no animation. Include 1440px, 375px, and 320px in visual checks; also check the existing tablet card grid when changing figure styles.
