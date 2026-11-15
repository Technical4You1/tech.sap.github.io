# Design brief

A site for Kashif Raza, an SAP Basis consultant with three years on SAP HANA,
S/4HANA and ECC landscapes. It is read by two kinds of visitor: an SAP team or
recruiter checking the work, and a Basis administrator after a runbook or a
freelance hand. It leads with the systems, not with a headshot.

What separates it from a consultant page is the evidence. The first screen is a
coded landscape status panel. The portfolio states scope, versions and outcome.
The free runbooks sit in the main path, not behind a form.

## Palette

Every value lives in `src/theme.css`. Nothing hardcodes a colour, a font stack,
a radius or a shadow — change the token and every component follows.

- **White ground** with **navy ink** (`--foreground`), and navy as a whole band
  for the top bar, the home hero and the library's premium list.
- **Blue** (`--primary`) carries every action and link, and nothing decorative.
- **Gold** appears only on premium labels — the badge, the request link, the
  premium eyebrow. Nowhere else on the site.
- **Green** (`--success`) marks a free runbook and a healthy system.
- **Pale blue-grey** (`--card`) holds panels and sample figures.

One colour scheme, deliberately. There is no `prefers-color-scheme` override.

The ground alternates and no section repeats the shape of the one before it:
navy hero → white facts row → panel skills → white case rows → panel strip.

## Type

IBM Plex — one family with an engineering voice, which suits a Basis
administrator's documents.

- `--font-heading` IBM Plex Sans Condensed, 500/600 — headings and numerals.
- `--font-body` IBM Plex Sans, 400/500/600 — running text.
- `--font-label` IBM Plex Mono, 400/500 — system identifiers, SIDs, version
  numbers, dates, status labels and eyebrows.

Loaded together in `src/fonts.css`. Changing a face means changing the import
and the token together.

## Layout

Dense on the library and the portfolio, airy on the home hero. One content
measure of 1180px, a fluid gutter, and `--section-space` between bands.

## Shell

A navy top bar on every route: the KR mark at the left, the five sections next,
a gold-rimmed Premium link, then the WhatsApp button in blue. At 360 the links
move into a sheet with a visible close and the message button stays. The footer
is a white band with the mark, the direct links and a photograph credit when one
exists.

## Brand mark

`src/components/Brand.tsx` is a KR monogram set in the heading face, white on
navy, in a rounded square with a blue system light at its top-right corner,
drawn in code. No logo file was supplied, so no logo is used. It appears in the
top bar, the sheet, the footer and — as a lettered shape in the same colours —
in `public/favicon.svg`.

Icons are lucide at **strokeWidth 1.5** throughout, and that is the only weight
the site uses. System status is shown with a dot of colour, not an icon.

## Imagery

No portrait or photograph of Kashif was supplied, so none is used and no stock
photograph is added. The space a picture would fill is held by the coded
landscape panel on the home page and by version-path and landscape diagrams on
the portfolio — divs, meters and SVG-style figures composed from the tokens.
Any picture that does appear is a real system screenshot supplied by the owner,
never a mood photograph.

## Voice

First person, plain, technical. Real versions and dates. No invented prices,
awards or testimonials. Sample figures inside the landscape panel are labelled
as a sample in the caption.
