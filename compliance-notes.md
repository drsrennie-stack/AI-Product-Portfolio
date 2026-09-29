# Compliance Notes: Product Portfolio

## 1. Project, files, date

- Project: Product Portfolio (NSF ATE Co-PI supporting page)
- Files covered: index.html
- Date: September 28, 2026 (icon grid layout, MedMasters house system)

## 2. WCAG version and level by criterion

Target: WCAG 2.2 AA minimum, AAA where achievable. Automated check: axe-core 4 (WCAG 2.0, 2.1, 2.2 A and AA plus best practices), zero violations at 320 px and 1280 px.

| Criterion | Level | How it is met |
|---|---|---|
| 1.1.1 Non-text content | A | Icons are decorative (aria-hidden); every tool's name is real text under its icon |
| 1.3.1 Info and relationships | A | Landmarks; one h1, an h2 for each group; each group's tools are a list |
| 1.4.3 / 1.4.6 Contrast | AAA | All text 7:1 or higher (section 3) |
| 1.4.4 Resize text | AA | Relative units; Larger text option raises the base from 18 px to 21 px |
| 1.4.8 Visual presentation | AAA (partial) | Left aligned, 68 character line cap, line height 1.65; More spacing option |
| 1.4.10 Reflow | AA | No horizontal scroll at 320 px (tested) |
| 1.4.11 Non-text contrast | AA | Icon tiles 18:1 (navy) and 7.66:1 (terra) on white; control borders 4.74:1 |
| 1.4.13 Content on hover or focus | AA | The description box opens on hover AND keyboard focus; the pointer can move onto the box without it closing; Escape closes it; it stays until the pointer or focus leaves |
| 2.1.1 Keyboard | A | Every tool is a native link; Tab moves through them and opens each description |
| 2.4.1 Bypass blocks | A | Skip link first |
| 2.4.4 Link purpose | A | Link text is the tool name plus "(opens in a new tab)" |
| 2.4.7 / 2.4.13 Focus visible and appearance | AAA | 3 px terra outline, 3 px offset |
| 2.5.5 Target size | AAA | Each tile is well over 44 by 44 px |
| 3.2.4 Consistent identification | AA | Every tile has the same parts in the same order |
| 4.1.2 Name, role, value | A | Toggles use aria-pressed; each tile link is described by its description box (aria-describedby) |
| 4.1.3 Status messages | AA | role="status" announces toggle changes and citation copies |

## 3. Color contrast audit

| Pair | Ratio | Result |
|---|---|---|
| Navy #0B1530 on white | 18.04:1 | AAA |
| Terra #8B3A2E on white | 7.66:1 | AAA |
| White on navy icon tile | 18.04:1 | AAA |
| White on terra icon tile | 7.66:1 | AAA |
| Gold #DCB45C on navy-deep #060C1E (faculty icons) | 9.94:1 | AAA |
| Muted #4F576A on white | 7.23:1 | AAA |
| Navy on navy-tint #EEF0F4 (tile hover) | 15.81:1 | AAA |
| Gold #DCB45C on navy (band) | 9.21:1 | AAA |
| #C9CEDA on navy-deep (footer) | 12.35:1 | AAA |

Group color (terra, navy, navy with gold) is never the only signal. Every group has a written heading.

## 4. Screen readers, touch, and cognitive access

- Screen readers hear each tool's name, then its full description, from aria-describedby, whether or not the box is on screen.
- Touch screens have no hover, so on phones and tablets the box is replaced by a one-line summary printed under each tool name.
- One short instruction line tells readers how the tiles work. It appears once, above the first group.
- Plain language, no italics, no justified text, no motion, and no carousel or hidden paging.
- Citations are in a collapsed "Citations for reviewers" section (native details element) with one Copy all button.

## 5. Keyboard flow

Skip link, Larger text, More spacing, each tool tile in reading order (its description opens on focus), Citations toggle, Copy all citations, footer link.

## 6. Screen reader testing

Automated: axe-core, zero violations. By hand still to do: VoiceOver on Safari and NVDA on Firefox. Confirm each tile reads its name, "opens in a new tab", and then its description.

## 7. Known limitations

- Tools with no confirmed link (blood gas app, simulated patient) are held in the data list and do not show until a link is added.
- On a touch device with a keyboard attached, the one-line summary shows instead of the box. The full description is still read by screen readers.
- Linked tools are covered by their own compliance notes.

## 8. Reviewer

Built and checked by Claude (Cowork session). Final review: Dr. Sharilyn Rennie.
