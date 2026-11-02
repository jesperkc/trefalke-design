---
name: Trefalke
description: A dimensioned drawing sheet, at page scale — the brand built out of the drafting grammar the bag builder's solver already speaks.
colors:
  paper: '#F5F2EA'
  ink: '#12333F'
  secondary: '#4F666F'
  line-thin: 'rgba(18, 51, 63, 0.42)'
  line-faint: 'rgba(18, 51, 63, 0.22)'
  scrim: 'rgba(18, 51, 63, 0.30)'
  taped: '#12333F'
  derived: '#0C7D5B'
  assumed: '#7A5100'
typography:
  display:
    fontFamily: "'Caveat', 'Barlow Semi Condensed', Arial, sans-serif"
    fontSize: 'clamp(2.4rem, 9vw, 6rem)'
    fontWeight: 600
    lineHeight: 0.95
    letterSpacing: '-0.03em'
    textTransform: 'none'
  figure:
    fontFamily: "'Barlow Semi Condensed', 'Helvetica Neue', Arial, sans-serif"
    fontSize: 'var(--gc-letter)'
    fontWeight: 600
    letterSpacing: '0.01em'
    fontVariantNumeric: 'tabular-nums'
  body:
    fontFamily: "'Barlow Semi Condensed', 'Helvetica Neue', Arial, sans-serif"
    fontSize: '1.0625rem'
    fontWeight: 400
    lineHeight: 1.5
  note:
    fontFamily: "'Barlow Semi Condensed', 'Helvetica Neue', Arial, sans-serif"
    fontSize: '0.8125rem'
    fontWeight: 400
    lineHeight: 1.4
  label:
    fontFamily: "'Barlow Semi Condensed', 'Helvetica Neue', Arial, sans-serif"
    fontSize: 'calc(var(--gc-letter) * 0.5)'
    fontWeight: 600
    letterSpacing: '0.03em'
  nav:
    fontFamily: "'Barlow Semi Condensed', 'Helvetica Neue', Arial, sans-serif"
    fontSize: '0.8125rem'
    fontWeight: 600
    letterSpacing: '0.11em'
    textTransform: 'uppercase'
  display-narrow:
    fontFamily: "'Barlow Condensed', 'Barlow Semi Condensed', Arial, sans-serif"
    fontSize: 'clamp(2rem, 11vw, 3.4rem)'
    fontWeight: 600
    lineHeight: 0.9
    letterSpacing: '-0.02em'
    textTransform: 'uppercase'
  display-short:
    fontFamily: "'Barlow Condensed', 'Barlow Semi Condensed', Arial, sans-serif"
    fontSize: 'clamp(1.75rem, 5.5vh, 2.6rem)'
    fontWeight: 600
    lineHeight: 0.9
    letterSpacing: '-0.02em'
    textTransform: 'uppercase'
  body-compact:
    fontFamily: "'Barlow Semi Condensed', 'Helvetica Neue', Arial, sans-serif"
    fontSize: '0.9375rem'
    fontWeight: 400
    lineHeight: 1.5
  nav-drawer:
    fontFamily: "'Barlow Semi Condensed', 'Helvetica Neue', Arial, sans-serif"
    fontSize: '1rem'
    fontWeight: 600
    letterSpacing: '0.09em'
    textTransform: 'uppercase'
  colophon-end:
    fontFamily: "'Barlow Semi Condensed', 'Helvetica Neue', Arial, sans-serif"
    fontSize: '0.75rem'
    fontWeight: 400
    letterSpacing: '0.08em'
    textTransform: 'uppercase'
  balloon:
    fontFamily: "'Barlow Semi Condensed', 'Helvetica Neue', Arial, sans-serif"
    fontSize: '10px'
    fontWeight: 600
    fontVariantNumeric: 'tabular-nums'
rounded:
  none: '0'
  focus: '1px'
  scrollbar: '5px'
  scrollbar-root: '6px'
  balloon: '9px'
spacing:
  gutter: 'clamp(18px, 2.6vw, 38px)'
  rule: '18px'
  title-inset: 'clamp(16px, 2.4vw, 34px)'
  corner-inset: 'clamp(18px, 3vh, 34px)'
components:
  button-primary:
    backgroundColor: '{colors.ink}'
    textColor: '{colors.paper}'
    rounded: '{rounded.none}'
    padding: '14px 20px'
    typography: '{typography.body}'
  button-primary-hover:
    backgroundColor: '{colors.derived}'
    textColor: '{colors.paper}'
  button-primary-active:
    backgroundColor: '{colors.derived}'
    textColor: '{colors.paper}'
  nav-link:
    textColor: '{colors.secondary}'
    typography: '{typography.nav}'
    padding: '0 0 2px'
  nav-link-current:
    textColor: '{colors.ink}'
    typography: '{typography.nav}'
  icon-button:
    textColor: '{colors.ink}'
    size: '38px'
    rounded: '{rounded.none}'
  icon-button-coarse:
    textColor: '{colors.ink}'
    size: '44px'
  cart-count:
    backgroundColor: '{colors.ink}'
    textColor: '{colors.paper}'
    rounded: '{rounded.balloon}'
    height: '17px'
    padding: '0 4px'
  drawer-panel:
    backgroundColor: '{colors.paper}'
    textColor: '{colors.ink}'
    rounded: '{rounded.none}'
    width: 'min(420px, calc(100vw - 48px))'
  drawer-title:
    textColor: '{colors.ink}'
    typography: '{typography.nav}'
  dimension-figure:
    textColor: '{colors.taped}'
    typography: '{typography.figure}'
---

# Design System: Trefalke

## Overview

**Creative North Star: "The Geometry Chart"**

Trefalke's visual world is not styled to resemble a technical drawing; it is
built out of one. The bag builder's solver already produces a dimensioned
frame drawing, and that drawing — datum mark, extension and witness lines,
arrowheads, section hatch, ground symbol — is the brand's
entire material vocabulary. A surface in this world is a sheet: full bleed,
dark on light, made of line, closed by hairline rules rather than by boxes.
Nothing is decorated into looking precise, because the thing on the page is the
precision.

One register, not two. The persuading surfaces and the working surfaces speak
the same way, because a drawing is dark on light and the pattern that comes out
of the tool is dark on light. The slate did not become a dark theme — it became
the ink. Density is low and the paper is mostly empty; the composition works by
placing few marks exactly, not by filling a grid. There is no card, no panel, no
plate, no tile anywhere in the world.

The world is opt-in per route. A route joins it by exporting
`handle = {ground: 'paper'}`; `PageLayout` hoists the deepest matched route's
answer onto the shell as `data-ground`, and the masthead, page and colophon all
read one set of tokens from there. A route that says nothing keeps
`data-ground="studio"` and the ported Studio theme. **The Studio theme
(`app/styles/studio.css`) is migration scaffolding and an explicit
anti-reference**: Manuale, the teal/sage/ochre palette and the pill buttons are
evidence of what exists on the live Shopify theme, not authority over anything.
Nothing in this document describes it, and nothing new should borrow from it.

**Key Characteristics:**

- Drafting grammar as the material, not as a motif.
- Warm paper and slate ink; one register everywhere.
- Everything is line. Exactly one filled shape per sheet, and it is the button.
- Colour is a provenance system: taped, derived, assumed.
- Square corners, hairline rules, no cards and no shadows on the page.
- Full bleed. The sheet runs to the paper edge; the world owns its own gutters.
- Motion is one load-time drafting sequence and nothing else.

## Colors

A two-value world — warm paper and slate ink — with a three-token provenance
system laid on top of it, and no decorative colour at all.

### Primary

- **Slate Ink** (`{colors.ink}`): every object line, every letter, the masthead
  and colophon text, the wordmark's fill, and the one filled shape on a sheet
  (the button's ground). It is the only colour the page commits at area scale,
  and it commits it once.

### Secondary

- **Solver Green** (`{colors.derived}`): the provenance colour for a quantity the
  arithmetic gave back, and — the same value, doing the same job of "the system
  answered you" — the world's entire interaction colour. It is the focus-ring
  stroke, the button's hover / focus / active ground, the selection wash (at 18%
  alpha), and the masthead's accent token on paper. Outside those interaction
  states it is unspent on `/bags`, which has no derived quantity to mark.

### Tertiary

- **Assumption Ochre** (`{colors.assumed}`): a quantity the solver took as
  given rather than measured. Declared and currently unspent anywhere in the
  build — it is reserved for the bag builder's own surfaces, which have
  quantities of all three kinds to mark. It stays declared rather than deleted
  so that those surfaces inherit the same three answers in the same three
  colours instead of inventing a second set.

### Neutral

- **Cool Paper** (`{colors.paper}`): the ground of every paper-ground surface —
  the field, the masthead, the colophon, the drawer panel, the scrollbar track,
  and the lettering reversed out of the button.
- **Tinted Secondary** (`{colors.secondary}`): supporting text — the lede, the
  free-and-nothing-to-sign note, the masthead's resting nav links, the
  colophon's links. Tinted from the ink's own hue and clearing 5.5:1 on paper.
- **Extension Line** (`{colors.line-thin}`): witness and extension lines. Thin
  enough to read as measurement apparatus rather than as object.
- **Faint Line** (`{colors.line-faint}`): tube bodies, the sheet's bottom edge,
  and every hairline rule in the chrome (masthead rule, colophon rules, drawer
  head rule, drawer panel border).
- **Scrim** (`{colors.scrim}`): the wash behind an open drawer, and the resting
  colour of the viewport scrollbar thumb.

### Named Rules

**The Provenance Rule.** Every quantity on screen is one of exactly three things
and says which by its colour: `taped` (you measured it), `derived` (it falls out
of the arithmetic), `assumed` (the solver took it as given). A number that
cannot answer that question does not get lettered. `/bags` spends only `taped`,
because it shows only tape measurements — and it shows five, so it may not
letter a sixth quantity anywhere on the sheet.

**The Absent Red Rule.** Red is not in this palette and may not be introduced.
It already means "cut here" on the exported 1:1 pattern, and one colour may not
mean two things across a brand.

**The One Filled Shape Rule.** A sheet is all line except for exactly one filled
shape, and that shape is the primary button. It therefore needs no size, no
colour and no rule to be the thing the eye finishes on. This is a budget, not a
description: anything else that takes a fill spends it, and the button pays.

**The Never Grey Rule.** Secondary text is tinted from the ink's own hue. Grey
beside a coloured ink reads as a mistake.

## Typography

**Display Font:** Barlow Condensed 600 (falling back to Barlow Semi Condensed,
then Arial)
**Body / Figure Font:** Barlow Semi Condensed 400 and 600 (falling back to
Helvetica Neue, then Arial)

Both are self-hosted from `/public/fonts` as woff2 with `font-display: swap`,
and the 600 Condensed plus the 400 Semi Condensed are preloaded in `root.tsx`.
Self-hosting is not a preference: Hydrogen's CSP allows `default-src 'self'` and
would block a third-party font host outright.

**Character:** The condensed drafting alphabet and nothing else. Condensed is a
functional choice before it is a stylistic one — dimension text has to fit in
the gap between extension lines. Figures are `tabular-nums` throughout, set on
the page root so numerals stay in column wherever they land.

### Hierarchy

- **Display** (600, `clamp(2.4rem, 9vw, 6rem)`, line-height 0.9, `-0.02em`,
  uppercase): the sheet's own name, lettered into the top-left corner. 9vw
  reaches the 6rem ceiling at 1024px and holds the proportion below it; at
  ≤860px the ramp re-bases to `clamp(2rem, 11vw, 3.4rem)`. Sized against the
  viewport, because the sheet _is_ the viewport.
- **Figure** (600, `var(--gc-letter)`, `0.01em`): the dimension value. Its size
  is a property of the sheet, not of the object (see the Named Rule).
- **Body** (400, `1.0625rem`, line-height 1.5, `text-wrap: pretty`): the lede.
  Capped at `min(46ch, calc(100vw - 2 × gutter))` by its container. `<strong>`
  inside it goes to 600 and to full ink — the one place body copy takes the
  object-line colour.
- **Note** (400, `0.8125rem`, max 44ch): the qualifying line under the button,
  and the colophon's links (at `0.06em`).
- **Label** (600, `calc(var(--gc-letter) * 0.5)`, `0.03em`): the sheet's
  secondary drawing register — a caption or a piece name, sized off the same
  `--gc-letter` as the figure so it stays subordinate at every format. Declared
  and currently unused: `/bags` letters five figures and nothing else.
- **Nav** (600, `0.8125rem`, `0.11em`, uppercase): masthead links. The same
  register carries the drawer title at `0.14em`, the mobile drawer list at
  `1rem` / `0.09em`, and the colophon's closing line at `0.75rem` / `0.08em`.

### Named Rules

**The Sheet-Height Lettering Rule.** Lettering height belongs to the sheet, not
to the object — the same rule that makes a 1:1 view and a 1:5 detail letter
identically on paper. `--gc-letter` is declared once per format by the route,
already divided by that format's framing scale (33 drawing units ÷ scale), so a
figure lands at the same height on glass in landscape and in portrait. Never set
a figure size in drawing units and never reach for a breakpoint to shout it back
up; that is the sound of a drawing being scaled instead of re-laid.

**The Two Registers Rule.** A drawing has exactly two lettering registers and no
third: the figure is the quantity, the label names the scale. Nothing else
letters on the sheet. There is no kicker, no eyebrow, no subhead, no caption
above a heading.

**The Sheet-Title Rule.** A title is lettered into the sheet's top-left corner,
where a drawing sheet carries its own name. It is never stacked above the
drawing as a headline with a picture underneath it.

## Layout

**The ground contract.** The shell (`.tf-shell`) hosts the whole world's tokens
and publishes the active ground as `data-ground`. `studio` is the default — a
route that has not been ported says nothing and keeps the theme it already had.
`paper` is opted into by `export const handle = {ground: 'paper'}`. The chrome
owns no colour of its own; every rule in it resolves through `--tf-ground`,
`--tf-on-ground`, `--tf-on-ground-soft`, `--tf-ground-rule`, `--tf-ground-accent`
and `--tf-scrim`, which is what lets one masthead serve both grounds without
either looking borrowed.

**The sheet.** A paper-ground route is one sheet in one viewport, with no
sections and no scroll. `<main>` becomes a flex column on paper so it hands its
height down rather than absorbing it, and the sheet takes
`calc(100svh - var(--tf-mast-h, 88px))` with `overflow: hidden`. `100svh`, not
`100dvh`: a sheet sized to the dynamic viewport re-lays itself every time a
mobile address bar collapses. `--tf-mast-h` is only ever assigned in the ≤860px
query (76px, where the wordmark is at its clamp floor); above that width the
88px fallback in the `calc` is the operative value.

**Gutters and bleed.** The page sets `margin: 0; padding: 0` and manages its own
bleed — a drawing sheet that stops short of the paper edge is a picture of a
sheet. The horizontal inset for everything that is not the drawing is
`--gc-pad`: `clamp(18px, 2.6vw, 38px)`, shared by the page, the masthead, the
colophon and the drawer. Vertically the sheet has two insets: the title at
`clamp(16px, 2.4vw, 34px)` from the top, the action corner at
`clamp(18px, 3vh, 34px)` from the bottom.

**Measure.** `--tf-measure` is `1600px` on the paper ground and `none` on
studio. It is applied to the masthead row and both colophon rows, which centre
within it via `margin-inline: auto`. The sheet itself is _not_ capped — it runs
full bleed at every width.

**Breakpoints.**

- `max-width: 860px` — the format switch. The framing transform swaps to the
  portrait matrix, the lettering height swaps with it, the display ramp re-bases,
  the masthead nav collapses to the menu toggle, and the colophon row stacks.
- `max-height: 560px` — a short window. The note under the button is dropped and
  the lede shrinks to `0.9375rem`. When the lede and the action corner compete
  for the same bottom edge, the lede gives way: the button is what the page is
  for.
- `pointer: coarse` — declared last in the file on purpose, so it outranks the
  widths it is correcting. Icon buttons and the drawer close go to 44px, their
  glyphs to 22px, the cart balloon rides up with the icon, and the drawer list
  takes a 15px vertical padding floor. Screen size does not tell you what is
  pointing at the screen; an iPad at 1024px runs the landscape sheet on a touch
  surface.

**Two formats, re-laid rather than scaled.** A drawing office does not shrink an
A0 sheet to make an A4 one. There is one SVG with a fixed `viewBox` and
`preserveAspectRatio="xMidYMid slice"`; the framing is a CSS transform
(`--gc-cam` / `--gc-cam-tall`) computed by the route against each window's own
shape and swapped at 860px. `slice`, not `meet`, is the difference between a
sheet and a picture of one: `meet` pads dead paper around the drawing, `slice`
makes the drawing cover the sheet and crops the excess, which is what a window
onto a large drawing does. The landscape format shows the whole bicycle; the
portrait format crops in x to the dimensioned triangle and lets the wheels run
off both edges as arcs.

**Known gap.** Verified in-browser at 1440×900 and at portrait. Widths below
500px are unverified — the browser in this environment enforces a ~500px minimum
window — so the portrait format's behaviour on a narrow phone is inferred from
its transform, not observed.

## Elevation & Depth

This system is flat. There is no shadow anywhere on a sheet, no elevation ramp,
and no tonal layering — because there are no surfaces to layer. Depth is carried
entirely by **line weight and opacity**, the way a drawing carries it: the
bicycle is the faintest thing on the sheet at 0.15–0.18 opacity because it is
context, the frame opening is a 2.6-unit line at 0.5 because it is what the tape
measures, and the bag is a 4.4-unit line at full ink because it is the subject.
A reader knows what matters from how hard the pen pressed.

The single exception is the drawer, which is the only element in the world that
genuinely sits _off_ the page.

### Shadow Vocabulary

- **Drawer lift** (`box-shadow: -22px 0 46px -30px rgba(18, 51, 63, 0.55)`):
  offset and blurred so the panel reads as a sheet lifted off the page, tinted
  from the ink rather than black. Used on `.tf-drawer__panel` only.

### Named Rules

**The Line-Weight Depth Rule.** Depth is stated in pen weight and opacity, never
in shadow. If a thing needs to recede, draw it fainter; if it needs to dominate,
draw it heavier. A shadow on a sheet is a claim that paper has a third
dimension.

**The No-Plate Rule.** A surface is never established by giving it a background.
There are no cards, no panels, no plates and no tiles in this world. The only
container on the sheet is the sheet's own edge rule.

## Shapes

**Square, always.** `border-radius` is `0` on every structural element: the
button, the sheet, the drawer panel, the masthead. The only radii in the world
are functional and sub-pixel-scale — the 1px softening on the focus ring, the
9px that makes the cart count a balloon rather than a box, and the browser
furniture (6px scrollbar thumb, 5px inside the drawer).

**Edges are rules, not boxes.** Every boundary in the chrome is a single 1px
hairline in `{colors.line-faint}`: the masthead closes with one, the colophon
opens with one and closes its legal line with a second, the drawer's head is
divided by one, and the sheet's own bottom edge is one. Nothing is ever outlined
on all four sides.

**The drafting alphabet.** The recurring geometry of this world is a fixed set
of drawing marks, and new surfaces should compose from it rather than invent:

- **Datum mark** — four arms out of the origin, not two crossed lines, so it
  opens from its own centre.
- **Extension and witness lines** — 1.7 units, `{colors.line-thin}`, running
  from 12 units off the feature to 18 past the dimension line, never touching
  it. The gap is what says the drawing is measuring the object rather than
  adding to it.
- **Dimension line and arrowheads** — a 2-unit run in `{colors.taped}` at 0.8,
  closed by a 22-unit solid arrowhead at each end.
- **Section hatch** — 45° lines at 18-unit pitch, 1.8 weight, 0.26 opacity.
  Marks cut material as the subject without spending a fill.
- **Ground symbol** — a line with tick hatching at 36-unit pitch beneath it,
  growing out of the drawing's origin rather than in from a paper edge.
- **Construction line** — dashed `24 15`, broken in the middle to hold its own
  figure. A drawing breaks a line where its figure sits; it does not run the
  line through the numerals. The gap is measured off the lettering it has to
  clear, which makes it a per-format quantity: lettering height belongs to the
  sheet, so the same figure occupies roughly 45 drawing units on the landscape
  format and 84 on the portrait one. One gap sized for either is a collision on
  one and a hole in the line on the other, so the break is authored twice and
  swapped by the same query that swaps the framing.

### Named Rules

**The No-Ratio Rule.** If a surface in this world ever needs to state scale, it
states it as a drawn bar and never as a ratio. "1:1" is a claim about physical
size and the browser has no idea how big its pixels are; a bar is drawn in the
same millimetres as the object and is therefore true on any display. On a page
whose payoff is "print at 100%", a false scale claim is the worst available
error.

The `/bags` sheet carries no scale notation at all, and that is the rule's other
half: a scale bar earns its place on a drawing whose view changes, and this
sheet has one view. A bar shipped here briefly and was removed — it was a second
lettered mark on a sheet whose whole discipline is that it letters five figures
and nothing else. The instrument lives where it does real work: the 100 mm check
square on the pattern the bag builder exports, which is the one mark a maker is
actually told to measure.

## Components

### Buttons

- **Character:** the one filled shape on the sheet. It is a plate of ink with
  the lettering reversed out of it.
- **Shape:** square (`0` radius), no border, `14px 20px` padding, inline-flex
  with a 14px gap to its trailing arrow.
- **Primary:** ink ground, paper lettering, 600 weight at `1.0625rem`, `0.01em`.
  The trailing arrow is an inline 18px SVG at `opacity: 0.72`, never an icon
  font and never a glyph character.
- **Hover / Focus:** ground goes to Solver Green and the plate lifts
  `translateY(-1px)` over 220ms on the house arrival curve. Hover is wrapped in
  `@media (hover: hover)`; focus-visible carries the identical treatment,
  because a keyboard is asking the same question a pointer is.
- **Active:** ground goes to Solver Green, translate returns to 0. A finger gets
  its answer on the way down, and the press reads as a press — the plate takes
  the ink rather than lifting off it.
- **Secondary / ghost:** none exist. A second button on a sheet would break the
  fill budget; a secondary action is a link.

### Navigation

The masthead is the sheet's top edge, not a banner: one row, `18px` above and
`16px` below, closed by a single hairline. The wordmark is applied as a CSS mask
over `currentColor` (`clamp(96px, 9vw, 124px)`, aspect-ratio 293/122) rather
than drawn, so the one committed brand asset is reproduced exactly while its
fill follows whichever ground it lands on.

- **Links:** Nav register, resting in `{colors.secondary}` over a transparent
  1px bottom border.
- **Current / hover:** full ink, and the bottom border takes ink. Because that
  underline is also what marks the current page, the hover half is guarded
  behind `@media (hover: hover)` — on a tablet an unguarded hover leaves the
  last item tapped underlined for the rest of the visit, the interface asserting
  you are somewhere you are not.
- **Icon buttons:** 38px square, no background, 21px inline SVG, `opacity: 0.72`
  resting → 1 on hover. 44px / 22px under `pointer: coarse`.
- **Cart count:** a drawing's balloon, not a badge — a 17px-high ink ring with
  paper numerals at 10px, `tabular-nums`, 9px radius.
- **Mobile (≤860px):** the link row is replaced by a menu toggle and the icons
  push to the end; the links reappear inside the drawer as a stacked uppercase
  list at `1rem` / `0.09em`, each row divided by a hairline.

### Drawers

Cart, search and menu share one shell, so porting it ports all three. A drawer
is a sheet that slides in over the page — right-anchored,
`min(420px, calc(100vw - 48px))` wide, so a sliver of scrim always stays
tappable beside it and a phone can dismiss it without hunting for the close
control.

- **Panel:** ground and text taken from the route underneath, a 1px hairline on
  its left edge, the drawer-lift shadow, square corners.
- **Head:** titled like a title block — Nav register at `0.14em`, uppercase,
  with a 36px close button (44px coarse) at `opacity: 0.72`, divided from the
  body by a hairline.
- **Body:** scrolls internally with a thinned scrollbar coloured from the ground
  rule; the page behind is locked via `html:has(.tf-drawer.is-open)` at every
  width, not only on a phone.
- **Motion:** scrim crossfades over 300ms, the panel translates in over 380ms,
  both on the house arrival curve. `visibility` is delayed out by 300ms so the
  fade can finish. Under reduced motion all three drop to a 1ms transition.

### The Colophon

The footer is the sheet's bottom edge and reads as one: a hairline, the link
row, the social marks (19px inline SVGs at `opacity: 0.66` → 1), then a second
hairline and one closing uppercase line at `0.75rem` / `0.08em`. No columns of
headings nobody asked for. It is pinned to the foot by `flex: 1` on `<main>`,
never floating under a short page.

### The Dimension (signature)

The recurring custom component of this world, and the one to reach for whenever
a surface has a measured quantity to state. It is built, not placed: two witness
lines out of the feature, a dimension line between them, an arrowhead closing at
each end, and the value read along the run — rotated to the run's own angle and
flipped past ±90° so it is always the right way up. Its colour is its provenance
token, not a decision.

**The figure always stands outboard**, 24 units along the outward normal, on the
far side of its own dimension line from the thing being measured. Turning the
lettering upright and choosing which side of the line it sits on are two
different decisions, and tying them together is a bug that hides well: the flip
past ±90° used to carry the offset with it, so the two runs wound leftward — on
`/bags`, the top tube and the head tube — put their figures _inboard_ while the
other three stood outboard, with nothing on the sheet to explain the difference.

The one figure permitted inside the object is a construction line's own value,
which belongs _on_ its line; the line breaks to hold it. See Shapes.

### The Drafting Sequence (signature motion)

This world's one authored moment: the drawing draws itself, once, on load, in
two acts. **Act one** is a draughtsman's hand, overlapped throughout — datum,
ground, bicycle, the four tubes as one circuit around the triangle, the opening,
then the bag under its hatch. **Act two** is the count: each dimension assembled
in 250ms and then held, alone and finished, for a 300ms beat before the next
witness line goes out. The beat is longer than the build on purpose — a stagger
shorter than a build overlaps, and overlapping is what act one does.

- **Two primitives.** `.tf-un__draw` strokes a mark along its own length
  (`stroke-dasharray: var(--gc-len)`, animating `stroke-dashoffset` from the
  full length to the element's own `0`). `.tf-un__arrive` fades a mark in from
  `opacity: 0` — for the marks a hand _places_ rather than strokes: arrowheads,
  figures, section hatch, ground hatching, and the dashed construction line,
  which has no choice since its dasharray is already spending itself on being
  dashed.
- **Cues come from the route.** `--gc-len`, `--gc-at` and `--gc-for` are handed
  in per element as inline custom properties, because the geometry already knows
  the run lengths and fifty cues written as fifty CSS rules is a sequence nobody
  can read. The stylesheet owns _how_ a mark draws; the drawing owns _when_.
- **Only `from` is declared** in each keyframe. A CSS animation with no `to`
  interpolates to the element's own underlying value, so an arrowhead at
  `opacity="0.9"` arrives at 0.9 and the sheet's static values stay the sheet's.
- **Nothing is gated behind it.** The static state is the finished drawing; a
  failed stylesheet or a late paint gives the same correct sheet, and the lede
  and button are painted and clickable at 0ms.

### Browser Surfaces

The browser's own furniture belongs to the design.

- **Selection:** Solver Green at 18% with ink text.
- **Focus ring:** `2px solid {colors.derived}`, `3px` offset, `1px` radius.
- **Scrollbar:** declared at `html:has(.tf-shell[data-ground='paper'])` with
  `color-scheme: light`, an 11px track in paper and a thumb in
  `{colors.scrim}` (→ `{colors.secondary}` on hover). The selector has to reach
  the root: the viewport scrollbar is propagated from `html`, and a descendant
  selector only reaches scrollbars _inside_ the shell. The values here are
  literal rather than `var(--gc-*)` for the same reason — the tokens live on
  `.tf-shell`, which is below the root.

### Named Rules

**The Pointer Rule.** Any hover treatment that changes state-bearing colour or
position is wrapped in `@media (hover: hover)`, and `:focus-visible` carries the
identical treatment. Hover is a pointer's answer and a finger has none; left
unguarded, a tap leaves the primary action of the page stuck mid-gesture.

**The Two Curves Rule.** This world has one ease —
`cubic-bezier(0.16, 1, 0.3, 1)`, the house arrival curve, on every transition,
fade and slide (180ms for text and opacity, 220ms for the button, 300–380ms for
the drawer) — and exactly one exception. A travelling stroke uses
`cubic-bezier(0.4, 0.08, 0.25, 1)`. The arrival curve spends 45% of its distance
in the first 11% of its time, which is right for a figure that should be where
it belongs before you finish noticing it moved, and wrong for a dash: the line
snaps most of the way out and then crawls the last inch, which reads as an
effect applied to a finished drawing rather than a drawing being made. A pen has
mass and leaves at a speed.

**The Reduced-Motion Rule.** Reduced motion gets a _different_ drawing, not a
disabled one. `animation: none` reads the preference as "no animation" rather
than "no motion" and leaves the visitor who asked for less movement with the one
page whose subject never arrives at all. What is objectionable is spatial: the
marks stop travelling and the dasharray is cleared with them, and the sheet
fades up once as a whole in 420ms on the arrival curve. Keep the arrival, drop
the travel.

## Do's and Don'ts

### Do:

- **Do** opt a route into this world explicitly with
  `export const handle = {ground: 'paper'}`. That is the whole switch, and it is
  the only one.
- **Do** spend exactly one fill per sheet, on the primary action. Everything
  else is line.
- **Do** colour every stated quantity by its provenance — `{colors.taped}`,
  `{colors.derived}`, `{colors.assumed}` — and letter no quantity that cannot
  answer which of the three it is.
- **Do** set lettering height per format on the sheet (`--gc-letter`), already
  divided by that format's framing scale, so a figure is the same size on glass
  in every orientation.
- **Do** re-lay a drawing for a second format by swapping its framing transform,
  never by scaling one sheet down.
- **Do** state scale as a drawn bar in millimetres, placed inside the region its
  own format actually shows.
- **Do** carry depth in line weight and opacity: faint for context, thin for the
  measured feature, heavy for the subject.
- **Do** close a region with a single hairline in `{colors.line-faint}`.
- **Do** guard state-bearing hover behind `@media (hover: hover)` and give
  `:focus-visible` the same treatment.
- **Do** inline every icon as SVG at 18–22px with `currentColor`.
- **Do** self-host any new face and preload the weights in use — Hydrogen's CSP
  (`default-src 'self'`) blocks third-party font hosts outright.
- **Do** let the static state be the finished artefact, so a failed stylesheet
  or a late paint still gives a correct sheet.

### Don't:

- **Don't** introduce red, in any tint. It means "cut here" on the exported
  pattern and may not mean anything else.
- **Don't** put a second filled shape on a sheet, or reverse a plate out of the
  ink to make a title block. The button is the budget.
- **Don't** wrap content in a card, panel, plate or tile, and don't establish a
  region by giving it a background.
- **Don't** add a `border-radius` above 0 to anything structural.
- **Don't** use shadows for depth on a sheet. The drawer's lift is the only
  shadow in the world.
- **Don't** use grey for secondary text; tint it from the ink's hue.
- **Don't** letter a third register. No kickers, no eyebrows, no subheads, no
  captions stacked above a heading — the figure and the label are the two, and
  there is no third.
- **Don't** stack a headline above a drawing. A title is lettered into the
  sheet's top-left corner.
- **Don't** gutter or inset a sheet. This world is full bleed and manages its
  own padding; a sheet that stops short of the paper edge is a picture of a
  sheet.
- **Don't** introduce scroll-driven motion. There is one load-time sequence and
  nothing else.
- **Don't** put the house arrival curve on a travelling stroke, or the stroke
  curve on anything that arrives.
- **Don't** answer `prefers-reduced-motion` with `animation: none`. Keep the
  arrival and drop the travel.
- **Don't** size a full-height surface with `100dvh`; use `100svh`, so a
  collapsing mobile address bar cannot re-lay the drawing under the reader.
- **Don't** borrow anything from `app/styles/studio.css` — Manuale, the
  teal/sage/ochre palette, the pill buttons. It is migration scaffolding and an
  explicit anti-reference, kept only until each route is ported.
- **Don't** size touch targets off viewport width. Size them off
`pointer: coarse`; a 1024px iPad is a touch screen.
</content>

</invoke>
