# Compliance Notes: Product Portfolio

## 1. Project, files, date

- Project: Product Portfolio (NSF ATE Co-PI supporting page)
- Files covered: index.html
- Date: September 28, 2026 (rebuilt on the MedMasters house system)

## 2. WCAG version and level by criterion

Target: WCAG 2.2 AA minimum, AAA where achievable. Automated check: axe-core 4 (WCAG 2.0, 2.1, 2.2 A and AA rules plus best practices), zero violations at 320 px and 1280 px.

| Criterion | Level | How it is met |
|---|---|---|
| 1.1.1 Non-text content | A | No images. Arrow glyphs are aria-hidden. Each external link carries "(opens in a new tab)" as screen reader text |
| 1.3.1 Info and relationships | A | header, nav, main, footer landmarks; one h1, h2 per section, h3 per tool; tools are list items holding an article; facts use dl, dt, dd; contribution areas are an ordered list |
| 1.3.2 Meaningful sequence | A | DOM order matches visual order |
| 1.4.3 / 1.4.6 Contrast | AAA | Every text pair is 7:1 or higher. See section 3 |
| 1.4.4 Resize text | AA | Relative units; works at 200 percent zoom. A Larger text option raises the base size from 18 px to 21 px |
| 1.4.8 Visual presentation | AAA (partial) | Left aligned, never justified; line length capped at 68 characters; line height 1.65; a More spacing option raises line height to 1.9 and adds letter and word spacing |
| 1.4.10 Reflow | AA | Single column at 320 px with no horizontal scroll (tested) |
| 1.4.11 Non-text contrast | AA | Button and toggle borders #6D7383 at 4.74:1; focus ring terra at 7.66:1 |
| 1.4.12 Text spacing | AA | Layout holds with the More spacing option on |
| 2.1.1 / 2.1.3 Keyboard | AAA | Every control is a native link or button |
| 2.3.3 Animation from interactions | AAA | No animation; smooth scroll turns off under prefers-reduced-motion |
| 2.4.1 Bypass blocks | A | Skip link is the first Tab stop |
| 2.4.4 / 2.4.9 Link purpose | AAA | Every "Open" link names its tool in screen reader text; every Copy citation button names its tool in its accessible name |
| 2.4.6 / 2.4.10 Headings and labels | AAA | Section headings on every part of the page |
| 2.4.7 / 2.4.13 Focus visible and appearance | AAA | 3 px terra outline with 3 px offset; gold outline on the navy footer |
| 2.5.3 Label in name | A | Accessible names start with the visible label |
| 2.5.5 Target size | AAA | Every button and link is at least 44 px tall |
| 3.1.5 Reading level | AAA (goal) | Plain sentences, one idea per sentence, no jargon without context |
| 3.2.3 / 3.2.4 Consistent navigation and identification | AA | Every tool card has the same layout and the same button labels |
| 4.1.2 Name, role, value | A | Reading option toggles use aria-pressed |
| 4.1.3 Status messages | AA | role="status" live region announces toggle changes and citation copies |

## 3. Color contrast audit

| Text / background | Ratio | Result |
|---|---|---|
| Navy #0B1530 on white | 18.04:1 | AAA |
| Terra #8B3A2E on white (eyebrows, accents, labels) | 7.66:1 | AAA |
| White on terra (primary buttons) | 7.66:1 | AAA |
| White on terra-deep #6E2C22 (button hover) | 10.26:1 | AAA |
| Muted #4F576A on white | 7.23:1 | AAA |
| Navy on navy-tint #EEF0F4 (hover) | 15.81:1 | AAA |
| White on navy (statement band, active toggle) | 18.04:1 | AAA |
| Gold #DCB45C on navy (band emphasis) | 9.21:1 | AAA |
| #C9CEDA on navy-deep #060C1E (footer small text) | 12.35:1 | AAA |
| Control borders #6D7383 on white | 4.74:1 | Passes 3:1 non-text |

Card borders (navy at 15 percent) are decorative. Card edges are also marked by spacing and headings, so 1.4.11 does not apply. Terra must never be lightened for text, since 7.66:1 is close to the AAA line.

## 4. Cognitive and neurodivergent design

- A "This page at a glance" summary sits at the top in three plain bullets.
- A "Go to a section" menu lets readers jump rather than scroll.
- Every tool card follows the same order: type, name, what it does, who it is for, what it shows, then actions.
- No italics anywhere (font-style forced to normal), no all-caps sentences (caps are used only for short labels), no justified text, no motion, no autoplay.
- Reading options for larger text and more spacing, remembered on the reader's own device only.
- Fonts: Plus Jakarta Sans for body text (open letterforms, plain zero) and Open Sans for headings, each with a sans-serif fallback.
- The page respects prefers-contrast (stronger borders and darker muted text) and forced colors (Windows High Contrast).

## 5. Keyboard navigation flow

Skip link, Larger text, More spacing, five section links, then for each of the 14 tools: Open link, then Copy citation (the Lab Practical card adds Station cards in between), then the footer link. Enter or Space activates each control. Verified in headless Chromium.

## 6. Screen reader testing

- Automated: axe-core, zero violations.
- Structural review: landmarks, heading outline, list counts, and accessible names checked in the DOM.
- Still to do by hand: VoiceOver on macOS Safari and NVDA on Windows Firefox. Confirm the heading rotor, the list count on each tool section, the aria-pressed state on the toggles, and the "Citation copied" announcement.

## 7. Known limitations and remediation

- Short uppercase labels (eyebrows, card type) use wide letter spacing. They are two to four words each and are not the only source of any information.
- In-page section links and the skip link do not carry target="_top", since that would reload the parent page when the portfolio is embedded.
- Tools linked from this page are covered by their own compliance notes.
- Manual screen reader pass pending (section 6).

## 8. Reviewer

Built and checked by Claude (Cowork session). Final review: Dr. Sharilyn Rennie.
