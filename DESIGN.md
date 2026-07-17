---
name: 2026 Training Programs
description: Shared weekly training tracker for a four-runner crew
colors:
  moss: "oklch(0.52 0.18 132)"
  moss-deep: "oklch(0.40 0.17 132)"
  race: "oklch(0.44 0.19 232)"
  race-deep: "oklch(0.30 0.16 232)"
  angela: "oklch(0.38 0.17 150)"
  angela-deep: "oklch(0.26 0.15 150)"
  taper: "oklch(0.42 0.16 68)"
  taper-deep: "oklch(0.28 0.14 68)"
  keyrace: "oklch(0.50 0.20 40)"
  recovery: "oklch(0.42 0.15 165)"
  build: "oklch(0.44 0.19 290)"
  peak: "oklch(0.40 0.18 6)"
  base: "oklch(0.38 0.02 132)"
  bg: "oklch(1.000 0.000 0)"
  surface: "oklch(0.965 0.006 132)"
  ink: "oklch(0.22 0.012 132)"
  muted: "oklch(0.48 0.014 132)"
  border: "oklch(0.88 0.008 132)"
typography:
  display:
    fontFamily: "-apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    fontSize: "23px"
    fontWeight: 800
    lineHeight: 1.2
    letterSpacing: "-0.02em"
  body:
    fontFamily: "-apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    fontSize: "13px"
    fontWeight: 400
    lineHeight: 1.5
  label:
    fontFamily: "-apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    fontSize: "11px"
    fontWeight: 700
    letterSpacing: "0.01em"
rounded:
  sm: "8px"
  md: "12px"
  lg: "16px"
  pill: "999px"
spacing:
  1: "4px"
  2: "8px"
  3: "12px"
  4: "16px"
  5: "24px"
  6: "32px"
  7: "48px"
components:
  tab-active:
    backgroundColor: "{colors.race}"
    textColor: "{colors.bg}"
    rounded: "{rounded.pill}"
    padding: "5px 16px 5px 5px"
  tab-inactive:
    backgroundColor: "{colors.bg}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    padding: "5px 16px 5px 5px"
  badge-lg:
    backgroundColor: "{colors.bg}"
    textColor: "{colors.race}"
    rounded: "999px"
    size: "56px"
  key-race-pill:
    backgroundColor: "{colors.keyrace}"
    textColor: "{colors.bg}"
    rounded: "{rounded.pill}"
    padding: "4px 11px"
  session-type-pill:
    backgroundColor: "{colors.race}"
    textColor: "{colors.bg}"
    rounded: "{rounded.pill}"
    padding: "2px 8px"
  week-row:
    backgroundColor: "{colors.bg}"
    textColor: "{colors.ink}"
    rounded: "{rounded.md}"
    padding: "8px 12px"
---

# Design System: 2026 Training Programs

## 1. Overview

**Creative North Star: "Trailhead, at full saturation"**

This is the third pass on the same idea: a trailhead at first light, before a long climb — moss green, trail-blaze amber, sunrise-cold-air energy. Pass one applied it as a light tint-swap (barely different from the original). Pass two made the colors bold but left the page structurally identical — same single-column stack, same flat undifferentiated list of 18 week rows. This pass fixes the actual complaint: the page is now a real two-column layout, and the week list is grouped into labeled, variably-sized training-phase blocks instead of one monotonous list. Color, component shape, *and* spatial structure now all carry the redesign.

Each runner keeps a monogram badge (S / A / G / X) instead of an illustrated mascot — a small geometric mountain-peak mark sits by the page title as a lightweight logo. Status icons (race flag, key-race star, team-race mark, taper arrow, coach-note bulb, taper checkmarks) are small inline SVGs, not emoji — emoji render inconsistently across platforms and read as an unfinished default, not a design decision.

This system explicitly rejects the corporate-SaaS-dashboard look (no gradient stat tiles, no BI-tool chrome) and the cream/sand AI-default surface (bg is pure white/near-black, never a warm tinted beige).

**Key Characteristics:**
- Real two-column grid ≥860px (272px sticky sidebar + main column), collapsing to a single stack below that — not a full-width column at every size
- The week list is grouped into labeled phase blocks (e.g. "Build · Wk 3–6") sized by how long that phase actually runs, not one flat list of identical rows
- Solid, saturated color fills on runner headers, the active tab, and every category pill — color carries real visual weight, not a tint
- Pure white / near-black page background; the boldness lives in the components, not the canvas
- Monogram badges (one letter, solid identity color, white type) replace illustrated icons; small inline SVG icons replace emoji throughout
- No side-stripe borders anywhere — session-type identification is a solid pill, matching the tag/badge language used everywhere else
- Flat by default — depth comes from color and tonal layering, never shadows
- One system-font stack throughout, carried by weight (800 for display, 700 for labels, 400 for body)

## 2. Colors

Full-palette strategy: 9 named roles (2 runner-only + 7 shared training-phase categories), each a solid, saturated fill — not a 4-8% tint. Every color must carry legible white text; that requirement, not a fixed lightness rule, is what tunes each value.

### Primary
- **Race** (oklch(0.44 0.19 232), dark oklch(0.62 0.17 232)): Star & Xavier's identity color and the "Race" training-phase category — active tab fill, header card, race-week rows and chips.
- **Race Deep** (oklch(0.30 0.16 232)): the gradient's dark end on Race-colored header cards.

### Secondary
- **Angela** (oklch(0.38 0.17 150)): Angela's identity color, a forest green distinct from Moss. Header card, active tab.
- **Taper** (oklch(0.42 0.16 68)): Gary's identity color and the "Taper" category — ochre/amber-brown.
- **Key Race** (oklch(0.50 0.20 40)): the one color reserved for urgency — key-race badges, the key-race week row's wash. A trail-blaze rust, deliberately distinct from Taper's ochre and Race's blue.

### Full Category Palette
Each training-phase category is a fully saturated, named color, used identically across all four runners' week badges, session-type pills, and the tag legend:
- **Recovery** (oklch(0.42 0.15 165)) — teal-green; a brighter variant (oklch(0.52 0.17 160)) marks "Team Race" weeks.
- **Build** (oklch(0.44 0.19 290)) — violet.
- **Peak** (oklch(0.40 0.18 6)) — rose-maroon.
- **Base** (oklch(0.38 0.02 132)) — warm neutral gray, low chroma by design (the "quiet" category).

### Neutral
- **Bg** (oklch(1.000 0.000 0) light / oklch(0.14 0.000 0) dark): the page background — pure, no tint.
- **Surface** (oklch(0.965 0.006 132) light / oklch(0.21 0.008 132) dark): session cards, coach notes, footer.
- **Ink** (oklch(0.22 0.012 132) light / oklch(0.94 0.008 132) dark): body text.
- **Muted** (oklch(0.48 0.014 132) light / oklch(0.66 0.012 132) dark): secondary text — week numbers, dates.
- **Border** (oklch(0.88 0.008 132) light / oklch(0.30 0.008 132) dark): hairline dividers only.

### Named Rules
**The Solid-Fill Rule.** Every category and identity color is a solid fill with white text, not a pale tint with colored text. A tint reads as decoration; a fill reads as a decision.

## 3. Typography

**Display Font:** -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif (one stack, weight does all the work)

**Character:** The title is now 800-weight with -0.02em tracking — a real logotype moment instead of a default heading. Body prose (session descriptions) moved from 12px to 13px/1.5 for comfort; compact UI chrome (dates, labels, badge counts) stays small and dense, since this is a scan-first data tool, not a reading surface.

### Hierarchy
- **Display** (800, 23px, -0.02em): the page title, set beside the logo mark.
- **Title** (800, 18px, -0.01em): runner names inside the header card.
- **Body** (400, 13px, 1.5): session descriptions.
- **Label** (700, 9.5–11px, 0.01em): badges, pills, week numbers, dates — bold at small sizes so they hold up as solid-fill chips.

### Named Rules
**The One-Family Rule.** Every weight in this system comes from the same font stack. Hierarchy is built with size and weight, never a second typeface.

## 4. Elevation

Flat by default, still. No shadows. The runner header cards use a subtle two-stop gradient (identity color → its deep variant) for a touch of dimensionality — a gradient *fill*, not a gradient *text* effect, and not a substitute for real depth cues elsewhere.

### Named Rules
**The Flat-by-Default Rule.** Surfaces never cast a shadow. The header card's gradient is the one deliberate exception to pure-flat, and it never appears on anything else.

## 5. Components

### Navigation (Tabs)
- **Shape:** pill (999px radius), monogram badge inline at the leading edge
- **Inactive:** white/bg background, 1.5px border, identity-colored badge (solid circle, white letter)
- **Active:** solid identity-color fill, white text, badge inverts to a white circle with identity-colored letter — contrast is maintained by inversion, not by changing the fill

### Monogram Badges
- **Small** (24px, tabs): solid identity color, white bold initial.
- **Large** (56px, header card): white circle, identity-colored initial — the inverse of the small badge, since it sits on the identity-colored header rather than on white.
- Replaces the previous illustrated zodiac-animal icon set entirely.

### Runner Header Card
- **Shape:** 16px radius, gradient fill (identity → identity-deep), white text throughout
- **Content:** large badge, name, race list, taper/recovery checkmarks — all white/white-90%

### Chips (Tag legend, race calendar, key-race badge)
- **Style:** solid category-color fill, white text, pill radius — no border, no tint
- **Count badges** (`.tc`): translucent white overlay circle on the pill, not a second solid color

### Session Type Pills
- Small solid-fill pill (category color, white text) at the top of each session card — replaces the previous `border-left` color stripe (an anti-pattern; side-stripes are banned outright). Same visual language as the tag legend, just smaller.

### Week Rows
- The week badge (`.wb`) is a solid-fill pill matching the category color, white text.
- **Past-week state:** reduced opacity (~0.4) with strikethrough.
- Rows are no longer one flat list — see Page Layout below.

### Page Layout
- **Structure:** `.ph` (runner header) is full-width above the fold as the one hero element. Below it, `.layout` is a 2-column CSS Grid at ≥860px (`272px 1fr`): a sticky `.sidebar` (tag legend, sparkline, race calendar — all demoted to compact, secondary-weight widgets) beside `.main` (the week list, the actual primary content, now getting the width it needs). Below 860px, `.layout` collapses to a single column and the sidebar unsticks.
- **Phase grouping:** `.wl`'s children are `.phase-group` blocks, not bare `.wr` rows. Each block gets a `.phase-head` label (solid category-color pill, e.g. "Build · Wk 3–6") sized to however many contiguous weeks share that category — real rhythm from real data, not decorative variation. Rows within a group keep a tight 4px gap; groups themselves get a generous 24px gap.
- **Named Rule: The Grouped-List Rule.** Any list long enough to need scanning (the week plan) must be chunked by a real semantic boundary (training phase) with a visible label, never left as one undifferentiated stack of near-identical rows.

## 6. Do's and Don'ts

### Do:
- **Do** use solid, saturated fills for every identity and category color — white text on top, not tinted-background-plus-colored-text.
- **Do** keep Bg pure white (light) / pure near-black (dark).
- **Do** use the monogram badge system (small on tabs, large+inverted on headers) consistently; never reintroduce per-runner illustrated icons.
- **Do** use a solid-fill pill for session type; never a colored border on any card.
- **Do** keep the gradient fill exception scoped to header cards only.
- **Do** use the 2-column grid + phase-grouped week list; both are load-bearing parts of this design, not optional flourish.
- **Do** use small inline SVG icons (currentColor, ~12px) for status glyphs (race flag, key-race star, team-race mark, taper arrow, coach-note bulb, checkmarks) — never emoji.

### Don't:
- **Don't** revert to pale tint chips/badges — that reads as decoration, not a decision, and was the exact complaint that triggered the color redesign.
- **Don't** flatten the week list back into one undifferentiated stack, and don't collapse the page back into a single full-width column at desktop widths — both were the exact complaint that triggered the layout redesign.
- **Don't** build a corporate-SaaS-dashboard look — no gradient stat tiles, no BI-tool chrome (per PRODUCT.md's anti-reference).
- **Don't** use `border-left`/`border-right` as a colored accent stripe anywhere (absolute ban) — use a solid pill, a filled background, or nothing.
- **Don't** introduce a cream/sand/beige tinted background.
- **Don't** pair a second typeface — one family, weight does the work.
- **Don't** use emoji for status glyphs — they render inconsistently across platforms and read as unfinished.
