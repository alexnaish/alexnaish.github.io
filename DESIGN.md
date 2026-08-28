---
name: naish.dev
description: A concise engineering decision record for Alex Naish.
colors:
  cobalt: "#155eef"
  cobalt-soft: "#e8efff"
  ink: "#171a1f"
  muted: "#5e6673"
  paper: "#ffffff"
  field: "#f2f5f9"
  rule: "#d6dce5"
typography:
  display:
    fontFamily: "Barlow, sans-serif"
    fontSize: "clamp(3.5rem, 7vw, 6rem)"
    fontWeight: 600
    lineHeight: 0.88
    letterSpacing: "-0.04em"
  display-compact:
    fontFamily: "Barlow, sans-serif"
    fontSize: "4rem"
    fontWeight: 600
    lineHeight: 0.88
    letterSpacing: "-0.04em"
  headline:
    fontFamily: "Archivo, sans-serif"
    fontSize: "clamp(1rem, 1.5vw, 1.25rem)"
    fontWeight: 500
    lineHeight: 1.3
    letterSpacing: "normal"
  title:
    fontFamily: "Archivo, sans-serif"
    fontSize: "clamp(1.5rem, 2.5vw, 2.25rem)"
    fontWeight: 500
    lineHeight: 1.15
    letterSpacing: "-0.025em"
  body:
    fontFamily: "Archivo, sans-serif"
    fontSize: "clamp(1rem, 1.5vw, 1.125rem)"
    fontWeight: 400
    lineHeight: 1.55
    letterSpacing: "normal"
  body-compact:
    fontFamily: "Archivo, sans-serif"
    fontSize: "clamp(0.95rem, 1.4vw, 1.075rem)"
    fontWeight: 400
    lineHeight: 1.45
    letterSpacing: "normal"
  label:
    fontFamily: "Fragment Mono, monospace"
    fontSize: "0.75rem"
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: "normal"
  label-compact:
    fontFamily: "Fragment Mono, monospace"
    fontSize: "0.7rem"
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: "normal"
rounded:
  none: "0"
  control: "2px"
spacing:
  xs: "8px"
  sm: "12px"
  md: "16px"
  lg: "24px"
  xl: "40px"
  xxl: "64px"
components:
  contact-link:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.paper}"
    typography: "{typography.label}"
    rounded: "{rounded.control}"
    padding: "12px 16px"
  contact-link-secondary:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
    typography: "{typography.label}"
    rounded: "{rounded.control}"
    padding: "12px 16px"
  evidence-row:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: "16px 0"
---

# Design System: naish.dev

## Overview

**Creative North Star: "Decision Record"**

The system borrows the clarity of contemporary engineering RFCs and architecture decision records without reproducing software chrome. It presents identity, verified expertise, and contact as one deliberate record: sparse enough to scan instantly, specific enough to feel authored.

The voice is modest, exact, and current. A cobalt review spine is the single memorable device; everything else serves reading order, contact, and confidence.

**Key Characteristics:**
- Clean white document field with graphite type
- One cobalt review spine and no decorative color scatter
- Large humanist-grotesk identity type with compact mono metadata
- Thin rules, square geometry, and no elevation
- Nearly one-screen composition with visible contact actions

## Colors

The strategy is restrained: neutral document surfaces carry most of the page, while cobalt marks review state and focus.

### Primary
- **Review Cobalt** (`colors.cobalt`): Review spine, active marks, focus rings, and selected text.
- **Review Wash** (`colors.cobalt-soft`): Quiet focus and emphasis fields where solid cobalt would dominate.

### Neutral
- **Graphite Ink** (`colors.ink`): Primary text and high-contrast actions.
- **Margin Note** (`colors.muted`): Secondary copy and metadata.
- **Document White** (`colors.paper`): Main reading field.
- **Workspace Field** (`colors.field`): Subtle page edge and mobile background separation.
- **Record Rule** (`colors.rule`): Dividers and structural hairlines.

### Named Rules

**The One-Mark Rule.** Cobalt belongs to the review spine, focus, and active state; do not scatter it as decoration.

**The Document Contrast Rule.** Keep core reading on Document White with Graphite Ink; secondary text must remain comfortably legible.

## Typography

**Display Font:** Self-hosted Barlow WOFF2 (with sans-serif fallback)
**Body Font:** Self-hosted Archivo WOFF2 (with sans-serif fallback)
**Label/Mono Font:** Self-hosted Fragment Mono WOFF2 (with monospace fallback)

**Character:** Barlow gives the name sturdy, even cap geometry; Archivo keeps supporting text calm and highly legible. Fragment Mono is restricted to record identifiers, field labels, and compact metadata.

### Hierarchy
- **Display** (600, fluid 3.5–6rem, 0.88): Alex's name only; uses the 4rem compact step below 760px and may wrap when user text-spacing settings require it.
- **Headline** (500, fluid 1–1.25rem, 1.3): Identity role.
- **Title** (500, fluid 1.5–2.25rem, 1.15): Evidence section heading.
- **Body** (400, fluid 1–1.125rem, 1.55): Positioning summary, capped near 65ch.
- **Body Compact** (400, fluid 0.95–1.075rem, 1.45): Evidence values.
- **Label** (400, 0.75rem, 1.4): Record labels, contact controls, and footer metadata.
- **Label Compact** (400, 0.7rem, 1.5): Evidence keys.

### Named Rules

**The Metadata Boundary Rule.** Mono type identifies structured fields; it never carries persuasive prose or becomes a technical costume.

## Layout

Desktop uses a twelve-column document grid inside one viewport-height field. Identity occupies the wider left area, with Alex's name held on one line when space permits; the evidence spine and factual record occupy the right. Contact actions remain adjacent to the identity rather than waiting at the page end. On narrow screens, the record becomes one direct vertical flow with unchanged reading order and no horizontal interaction.

Spacing follows an 8px-root rhythm with larger 24px, 40px, and 64px separations between semantic groups. The composition may breathe, but it must not become a long portfolio scroll.

## Elevation & Depth

The system is flat. Document boundaries, rules, and cobalt state changes create separation; shadows, glass, and floating panels are excluded.

**The Flat Record Rule.** Every element belongs to one document plane. Use rules and spacing, never elevation, to group information.

## Shapes

Geometry is square and exact. Rules are one pixel; controls use a restrained 2px radius for optical softness. The review marker may use a small circle because it represents a point on the evidence spine, not a decorative pill.

## Components

### Contact Links
- **Shape:** Compact rectangular actions with a 2px radius.
- **Primary:** Graphite fill with Document White text.
- **Secondary:** Document White with a Record Rule border.
- **Hover / Focus:** Cobalt becomes the active edge or fill; keyboard focus uses a visible offset cobalt outline.

### Evidence Spine
- **Structure:** Four verified skill groups aligned to one cobalt vertical rule.
- **State:** A single review pass brings markers into alignment on entry, then stops.
- **Content:** Frontend, backend, architecture, and platform capabilities grounded in the CV; do not imply unsupported outcomes.

### Record Metadata
- **Style:** Fragment Mono labels paired with Archivo values.
- **Use:** Location, profile type, and direct contact details.

## Do's and Don'ts

### Do:
- **Do** make identity, expertise, and contact visible within seconds.
- **Do** use the evidence spine as the only expressive system device.
- **Do** keep claims specific, verified, and modest.
- **Do** preserve full functionality when fonts, animation, or JavaScript fail.

### Don't:
- **Don't** turn the page into terminal cosplay, retro stationery, or a themed prop.
- **Don't** introduce card grids, dashboards, project metrics, or long-form sections without real evidence.
- **Don't** scatter cobalt across unrelated decoration.
- **Don't** invent employers, projects, testimonials, availability, or performance claims.
