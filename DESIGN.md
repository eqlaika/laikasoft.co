---
name: Laikasoft
description: A compact, dark utility index for EverQuest software and support.
colors:
  night-canvas: "#0a0a12"
  quiet-surface: "#12121e"
  hairline: "#1e1e30"
  primary-text: "#c8c8d4"
  muted-text: "#85859a"
  link-indigo: "#7b8cde"
  selection-indigo: "#4a5599"
typography:
  display:
    fontFamily: "SF Mono, Cascadia Code, Fira Code, monospace"
    fontSize: "clamp(1.5rem, 4vw, 1.85rem)"
    fontWeight: 600
    lineHeight: 1.25
    letterSpacing: "-0.02em"
  body:
    fontFamily: "-apple-system, Segoe UI, Helvetica, Arial, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.6
  title:
    fontFamily: "-apple-system, Segoe UI, Helvetica, Arial, sans-serif"
    fontSize: "1rem"
    fontWeight: 600
    lineHeight: 1.35
  label:
    fontFamily: "SF Mono, Cascadia Code, Fira Code, monospace"
    fontSize: "0.85rem"
    fontWeight: 500
    lineHeight: 1.6
spacing:
  compact: "0.5rem"
  content: "1.5rem"
  section: "2rem"
components:
  text-link:
    textColor: "{colors.link-indigo}"
    typography: "{typography.body}"
  navigation-link:
    textColor: "{colors.muted-text}"
    typography: "{typography.label}"
  support-route:
    backgroundColor: "{colors.night-canvas}"
    textColor: "{colors.primary-text}"
    padding: "1.5rem 0"
    width: "100%"
---

# Design System: Laikasoft

## Overview

**Creative North Star: "The quiet utility index"**

Laikasoft is a compact technical directory rather than a marketing stage. One narrow column, spare copy, and high-confidence text links make each page feel direct and maintained. The dark field supports late-night game and desktop use without adding fantasy decoration or dashboard chrome.

The system earns hierarchy through type register, spacing, and one-pixel divisions. Product art appears only when it carries identity; support and navigation remain typographic.

**Key Characteristics:**

- A near-black, single-column canvas with no ornamental panels.
- Cool grey text and one muted indigo action color.
- Monospace for product identity and actions; system sans for explanation.
- Short pages, plain language, and visible authoritative links.

## Colors

The palette is restrained: one cool indigo accent sits over adjacent blue-black and cool-grey neutrals.

### Primary

- **Link indigo** (`colors.link-indigo`): Links, current navigation, and keyboard focus. Its rarity keeps every accent actionable.
- **Selection indigo** (`colors.selection-indigo`): Text selection behind white text; it does not compete with ordinary links.

### Neutral

- **Night canvas** (`colors.night-canvas`): The site-wide page background.
- **Quiet surface** (`colors.quiet-surface`): Reserved tonal step for a surface that genuinely needs separation; do not introduce a panel merely to use it.
- **Hairline** (`colors.hairline`): One-pixel route and section divisions.
- **Primary text** (`colors.primary-text`): Headings and ordinary body copy.
- **Muted text** (`colors.muted-text`): Explanatory copy, navigation at rest, and footer details; it remains readable against the canvas.

**The Action Color Rule.** Link indigo means an element can be followed or focused. Do not scatter it onto decorative labels.

## Typography

**Display Font:** SF Mono / Cascadia Code / Fira Code with the generic monospace fallback  
**Body Font:** platform system sans (`-apple-system`, Segoe UI, Helvetica, Arial)  
**Label/Mono Font:** the same monospace stack as display

**Character:** Monospace marks Laikasoft identity and direct actions without making explanatory copy feel like a terminal. The system sans keeps instructions familiar and compact.

### Hierarchy

- **Display** (`typography.display`): Page titles; one per page, left aligned.
- **Title** (`typography.title`): Compact section and route headings.
- **Body** (`typography.body`): Descriptions and explanatory text, kept inside the 640px site measure.
- **Label** (`typography.label`): Direct support actions and compact navigation.
- **Utility text** (0.75–0.9rem): Navigation and footer context only; utility size is not a substitute for content hierarchy.

**The Two-Register Rule.** Monospace names the place or the action; system sans explains it.

## Layout

The site uses one centered column with a 640px maximum width. Navigation, main content, and footer share the same horizontal alignment and 1.5rem side padding. Main content receives 3rem of vertical padding; short pages let the flex layout hold the footer at the bottom of the viewport.

Support routes span the column and use a content/action split on wider screens. At 540px and below, each route becomes one column with its action directly under the explanation. Layout must remain naturally scrollable and free of horizontal overflow at 390px.

**The One-Column Rule.** Add hierarchy inside the shared measure before considering a second region or sidebar.

## Elevation & Depth

The system is flat. It uses adjacent dark tones and one-pixel hairlines, not shadows, glows, glass, or floating containers. Focus is an interaction outline rather than simulated elevation.

## Shapes

Rectangles stay structurally square. Dividers run edge to edge within the content measure. The only rounding in the current system is a subtle 2px radius on keyboard focus outlines; product imagery keeps its authored silhouette.

## Components

### Text links

- **Style:** Link indigo, no underline at rest, and a modest underline offset when hovered.
- **Focus:** A 2px link-indigo outline with 4px offset remains visible on the night canvas.
- **Language:** Labels name destinations or actions directly; decorative arrows are hidden from assistive technology.

### Navigation

- **Style:** A compact horizontal row inside the shared 640px measure. The Laikasoft mark uses monospace and the favicon; Stonemite carries its existing product icon.
- **State:** Inactive destinations use muted text. Hover and `aria-current="page"` change to link indigo.
- **Responsive behavior:** The row remains compact at mobile widths and must not force horizontal scrolling.

### Support routes

- **Structure:** A full-width row between one-pixel hairlines, with explanatory copy on the left and one action on the right.
- **Spacing:** 1.5rem vertically on wide screens and 1.35rem on narrow screens.
- **Motion:** The arrow moves 0.2rem over 160ms ease-out on hover; `prefers-reduced-motion` removes the transition.
- **Responsive behavior:** Below 540px, copy and action stack in reading order.

## Do's and Don'ts

### Do:

- **Do** keep pages concise enough that the next useful action is visible quickly.
- **Do** use semantic headings, descriptive links, `aria-current`, and visible keyboard focus.
- **Do** use product artwork only for real product identity.
- **Do** divide parallel choices with hairlines rather than wrapping each one in a card.

### Don't:

- **Don't** add fantasy-game ornament, neon glow, glass, or decorative gradients.
- **Don't** turn short support content into a dashboard, card grid, or simulated help centre.
- **Don't** use muted text below accessible contrast on the night canvas.
- **Don't** promise support channels, response times, or product claims that are not documented in PRODUCT.md.
