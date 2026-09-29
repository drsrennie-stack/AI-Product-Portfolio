# Compliance notes: Sharilyn Rennie Learning Systems Portfolio

## 1. Project, files, date

- Project: Learning Systems Portfolio (home page plus six project pages in one file)
- Files: index.html, img/ (31 screenshots, JPEG)
- Date: September 29, 2026

## 2. WCAG version and level targeted

WCAG 2.2, AA floor, AAA where achievable. Nothing here has been certified by an outside auditor.

| Criterion | Level reached | How |
|---|---|---|
| 1.1.1 Non-text content | AA | Every screenshot has descriptive alt text. Thumbnails and tile images are decorative (alt="") because the button or link carries the name. |
| 1.3.1 Info and relationships | AA | Landmarks (header, nav, main, footer), one h1 per view, h2 per section, h3 inside, ordered lists for steps. |
| 1.4.3 / 1.4.6 Contrast | AAA | All text pairs 7:1 or higher (table below). |
| 1.4.1 Use of color | AA | Selected screen uses a thicker border plus aria-pressed, not color alone. Review notes use a dashed border and a written label. |
| 1.4.10 Reflow | AA | Single column at 320 to 390 px, no horizontal scroll (checked at 390 px). |
| 2.1.1 Keyboard | AA | Every link, button, thumbnail and the lightbox work by keyboard. |
| 2.4.1 Bypass blocks | AA | Skip link to main content. |
| 2.4.3 Focus order | AA | Focus moves to the page h1 on every project change; lightbox moves focus to Close and returns it to the screenshot. |
| 2.4.7 / 2.4.13 Focus visible | AA | 3 px rust outline with offset on every interactive element. |
| 2.5.8 Target size | AA | Nav, buttons and thumbnails are at least 44 px tall. |
| 4.1.2 Name, role, value | AA | aria-pressed on the notes toggle and thumbnails; the lightbox is a native dialog with aria-labelledby. |
| 4.1.3 Status messages | AA | Screen changes and page changes are announced through aria-live regions. |
| 2.3.3 Animation from interactions | AAA | Card lift is the only motion and is turned off under prefers-reduced-motion. |

## 3. Color contrast audit

| Pair | Colors | Ratio | Result |
|---|---|---|---|
| Body text | #0B1530 on #FAFAF9 | 17.27:1 | AAA |
| Text on white cards | #0B1530 on #FFFFFF | 18.04:1 | AAA |
| Secondary text | #464D60 on #FAFAF9 | above 7:1 | AAA |
| Rust eyebrows and accents | #8B3A2E on #FAFAF9 | 7.33:1 | AAA |
| Rust on white | #8B3A2E on #FFFFFF | 7.66:1 | AAA |
| Button text | #FFFFFF on #8B3A2E | 7.66:1 | AAA |
| Button hover | #FFFFFF on #6E2C22 | 10.26:1 | AAA |
| Gold labels on navy band | #DCB45C on #0B1530 | 9.21:1 | AAA |
| White on navy band | #FFFFFF on #0B1530 | 18.04:1 | AAA |
| Secondary text on navy | #C4CAD6 on #0B1530 | 10.97:1 | AAA |

Contrast inside the screenshots belongs to each app. Known failures in the apps are listed in each project's review notes, and screens that showed them were left out.

## 4. Keyboard navigation flow

Checked with scripted Tab and Enter in Chromium: skip link, brand, Work, Approach, About, See the work, How I design, then the six project tiles. Enter on a tile opens the project and focuses its h1. On a project page: All projects, app link, screenshot (Enter opens the lightbox), thumbnails (Enter switches the screen), Previous and Next. Escape closes the lightbox and focus returns to the screenshot.

## 5. Screen reader testing

Not yet done with a real screen reader. Structure was checked in code: landmarks, heading order, alt text, aria-live announcements, aria-pressed states, and dialog labelling. Remediation: run VoiceOver (Safari, macOS) through the home page and one project page before publishing.

## 6. Known limitations and remediation plan

- Screen reader pass pending (see section 5).
- In-page project links do not use target="_top" because the site switches views with #links inside one page. If embedded in Kajabi, open it as a full page rather than in an iframe.
- Internal review notes were removed from the published version.
- Screenshots are images of other apps. Their internal contrast issues are tracked per project and should be fixed in the apps before the next screenshot pass.

## 7. Reviewer

Prepared by Claude for Dr. Sharilyn Rennie. Pending her review.
