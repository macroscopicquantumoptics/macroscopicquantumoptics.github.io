---
name: Macroscopic Quantum Optics
description: A clean lab group web page, clear and informative, with one consistent theme.
colors:
  school-of-science-yellow: "#F7E159"
  paper-white: "#FFFFFF"
  ink-black: "#000000"
  muted-grey: "#595959"
  muted-grey-dark: "#A6A6A6"
  hairline: "#D9D9D9"
  hairline-dark: "#333333"
  blank: "#F2F2F2"
  blank-dark: "#141414"
typography:
  display:
    fontFamily: "Inter, Arial, sans-serif"
    fontSize: "clamp(40px, 6vw, 72px)"
    fontWeight: 700
    lineHeight: 1.08
    letterSpacing: "-0.025em"
  headline:
    fontFamily: "Inter, Arial, sans-serif"
    fontSize: "clamp(26px, 3vw, 32px)"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: "-0.025em"
  title:
    fontFamily: "Inter, Arial, sans-serif"
    fontSize: "18px"
    fontWeight: 700
    lineHeight: 1.4
    letterSpacing: "-0.01em"
  body:
    fontFamily: "Inter, Arial, sans-serif"
    fontSize: "18px"
    fontWeight: 400
    lineHeight: 1.65
rounded:
  none: "0"
  switch: "18px"
spacing:
  gutter: "clamp(20px, 5vw, 80px)"
  row: "44px"
  section-title-gap: "48px"
  block: "144px"
  page-top: "128px"
  container: "1320px"
components:
  nav-link-current:
    textColor: "{colors.ink-black}"
    typography: "{typography.body}"
  link-hover:
    backgroundColor: "{colors.school-of-science-yellow}"
    textColor: "{colors.ink-black}"
    rounded: "{rounded.none}"
  mark:
    backgroundColor: "{colors.school-of-science-yellow}"
    textColor: "{colors.ink-black}"
    rounded: "{rounded.none}"
    padding: "0 0.12em"
  list-row:
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: "44px 0"
  theme-switch:
    backgroundColor: "{colors.paper-white}"
    textColor: "{colors.ink-black}"
    rounded: "{rounded.switch}"
    width: "72px"
    height: "36px"
---

# Design System: Macroscopic Quantum Optics

## Overview

**Creative North Star: "The Clear Lab Page"**

A clean lab group web page that is clear and informative, with one consistent theme on every page. The site follows the Aalto brand guidelines, the same rules as the group meeting slides, so the website, the slides and Aalto's own pages read as one family. Black type on white (white on black in dark mode), one typeface, three type sizes, and School of Science Yellow as the only colour.

Pages are lists of real things: research directions, people, papers, news, tools. Structure comes from white space, one left edge and 1px hairlines between items, never from boxes or decoration. The one exception is the home page picture: a dark band, in both themes, holding interactive 3D models of the group's own experiments, each linked to its paper.

Density is low and the measure is short (64ch). Nothing moves on its own except the home page models, and with reduced motion nothing does.

**Key Characteristics:**
- Black and white, with yellow only as a highlight.
- Inter Bold headings with tight tracking; Inter Regular for everything else.
- Three type sizes: page title, section title, body.
- Flat: no cards, shadows, gradients, rounded corners, chips or icons on links.
- One left edge; items separated by hairlines and white space.
- Light and dark themes, switched in the lower right corner.

## Colors

Strictly monochrome, with one yellow used as a highlighter, never as text or decoration.

### Primary
- **School of Science Yellow** (#F7E159): the Aalto School of Science colour and the only highlight. It marks the background of a hovered link, `<mark>` around a key phrase, the skip link, and the theme switch's knob. Text on yellow is always black, in both themes.

### Neutral
- **Paper White** (#FFFFFF): page background in light mode; text in dark mode and on the home page picture.
- **Ink Black** (#000000): text in light mode; page background in dark mode; the home page picture in both themes.
- **Muted Grey** (#595959 light, #A6A6A6 dark): dates, roles, authors, keywords, captions, footer text. Same size as body text, only greyer.
- **Hairline** (#D9D9D9 light, #333333 dark): the 1px rules between list items, above the footer, and around mostly-white screenshots.
- **Blank** (#F2F2F2 light, #141414 dark): the empty portrait placeholder for a person with no photo yet.

### Named Rules
**The Highlighter Rule.** Yellow is a background behind black text, never a text colour, border or fill on its own. If it isn't marking "you're pointing at this" or "this phrase matters", it isn't yellow. The current page in the nav is not yellow, so it never looks like a hovered link.

**The Token Rule.** Colours come from the variables at the top of `assets/site.css` (`--bg`, `--fg`, `--muted`, `--accent`, `--line`, `--blank`), redefined for dark mode. Don't write raw hex in a rule, except black text on yellow and the always-dark home page picture.

## Typography

**Display Font:** Inter Bold (with Arial)
**Body Font:** Inter Regular (with Arial)

**Character:** One family, two weights. Bold headings with tracking -25 read as Aalto's own voice; Regular body text is plain and easy to read.

### Hierarchy
- **Display** (700, clamp(40px, 6vw, 72px), 1.08): the page title, one per page. On the home page, kept to about 12 to 16 characters per line.
- **Headline** (700, clamp(26px, 3vw, 32px), 1.2): section titles and publication years.
- **Title** (700, 18px, 1.4): item names in lists (a person, a news item, a research direction). The same size as body, only bold, so it does not count as a fourth size.
- **Body** (400, 18px, 1.65; 17px under 600px): running text, at most 64ch per line. Dates, roles and authors use body size in Muted Grey, never smaller.

### Named Rules
**The Three Sizes Rule.** Page title, section title, body. No small print, captions or labels at a fourth size.

**The Sentence Case Rule.** Sentence case everywhere, no UPPER CASE, left-aligned, ragged right. Bold a person's name on its first mention in running text.

## Layout

One centred container (max 1320px) with a side gutter that grows with the window (clamp(20px, 5vw, 80px)). Everything starts on the same left edge; bulleted lists are indented further than their heading (28px).

Vertical rhythm is generous: 128px above the page title, 144px between major blocks, 48px under a section title, 44px of padding in each list row. Pages are single-column lists except where content earns columns: three research directions side by side on the home page, news with text left and a 320px picture right, publications with the year in a 140px column on the left, and a people grid of 220px-minimum portraits.

The header has the MQO logo top left, the navigation, and the Aalto logo in the top right corner. The MQO letters are the same height as the Aalto "A?".

**Responsive:** under 900px, both logos share the top row and the navigation drops below them; columns collapse to one; the home page picture becomes a 16:9 band under the header with the text below it. Under 600px, body drops to 17px, spacing tightens (72px page top, 96px between blocks, 36px rows), the people grid goes to two columns and the publication year sits above its papers.

## Elevation & Depth

None. The site is completely flat: no shadows, no layered surfaces, no gradients. Separation is a 1px hairline or white space. The only floating element is the theme switch, which sits above the page with a 1px outline, not a shadow.

### Named Rules
**The Hairline Rule.** If two things need separating, use 1px of `var(--line)` or more white space. Never a box, a tinted panel or a shadow.

## Shapes

Square corners everywhere: photos, figures, screenshots, highlights, the home page picture. Portraits are cropped to 3:4.

Circles appear only where the form is a dot by nature: list bullets (7px), the model-picker dots on the home page (8px), and the theme switch (a pill with an 18px radius and a round knob). These are the only exceptions to the no-rounded-corners rule.

## Components

### Links
- **Default:** inherit the text colour, 1px underline offset 0.18em.
- **Hover:** School of Science Yellow background, black text, underline removed. Headings that are links (names, research titles) drop the underline at rest.
- **Focus:** 2px solid outline in the text colour, 3px offset (white on the dark home page picture).
- **No icons or arrows** after links.

### Navigation
- **Style:** body-size Inter Regular, no underline, 36px gaps (20px on phones).
- **Hover:** 1px underline, no yellow.
- **Current page:** 2px underline in the text colour (`aria-current="page"`), 0.3em below the text like the hover underline. Quieter than the page title, and different from link hover.
- **Mobile:** wraps below the logo row under 900px.

### Lists (news, publications, research)
- **Rows:** separated by 1px hairlines top and bottom, 44px vertical padding.
- **Meta line:** date or role in Muted Grey, body size, above the title.
- **Publications:** title is the link in bold; authors, then journal, each on its own grey line.

### People grid
- **Portraits:** 3:4, square corners, Blank placeholder when there is no photo.
- **Hover / focus:** contact details appear over the lower edge of the photo on a page-colour strip with a hairline on top. Not shown on touch screens.

### Theme switch
- **Place:** fixed in the lower right corner, 72 x 36px pill with a 1px outline in the text colour.
- **State:** a School of Science Yellow knob slides under the sun (light) or moon (dark); the active icon is black, the other grey. No motion with reduced motion.

### Home page picture (signature)
- **Dark band** (#000 in both themes) holding the 3D models from `assets/hero3d.js`, with the page title and intro over it in white.
- **Model picker:** arrows either side of one 8px dot per model, centred at the bottom; the shown model's dot is filled. Hover turns them yellow.
- **Paper link:** grey (#A6A6A6) in the lower right corner, level with the content's right edge.
- **Fallback:** a looping video of the dark trap where WebGL is missing; the model fades in over 0.8s when ready.

## Do's and Don'ts

### Do:
- **Do** use the CSS variables (`--bg`, `--fg`, `--muted`, `--accent`, `--line`, `--blank`) so both themes work.
- **Do** separate list items with 1px `var(--line)` hairlines and white space.
- **Do** keep every block on the one left edge, with body text at most 64ch wide.
- **Do** use Muted Grey at body size for dates, roles, authors and captions.
- **Do** check every change in light mode, dark mode and at phone width.
- **Do** keep the Aalto logo whole: no cropping, recolouring (beyond the dark-mode inversion) or stretching.

### Don't:
- **Don't** put yellow text on white, or use yellow anywhere other than as a highlight behind black text.
- **Don't** add cards, boxes, shadows, gradients, rounded corners, chips, tags, or icons and arrows on links.
- **Don't** add a fourth type size or set text smaller than body.
- **Don't** use UPPER CASE, centred text or justified text.
- **Don't** introduce a second typeface, a second accent colour or a CDN-loaded asset.
- **Don't** make any area dark except the home page picture.
