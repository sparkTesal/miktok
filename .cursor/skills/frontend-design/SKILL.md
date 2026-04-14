---
name: frontend-design
description: Build distinctive, production-grade frontend interfaces for this project using its integrated Figma-inspired visual system. Use when implementing or restyling web components, pages, landing pages, dashboards, React components, HTML/CSS layouts, or when polishing any web UI.
license: Complete terms in LICENSE.txt
---

# Frontend Design

Use this skill to turn UI requests into polished, production-grade frontend code with a strong visual point of view.

## When To Apply

Apply this skill when the user asks to:

- Build or restyle a page, section, component, landing page, or dashboard
- Improve the visual quality of existing frontend code
- Translate product or marketing requirements into web UI
- Make a frontend feel more intentional, distinctive, and less generic

## Workflow

1. Read this skill and extract only the rules relevant to the task.
2. Identify the requested surface: hero, navigation, card, section, form, dashboard, or full page.
3. Preserve a single clear aesthetic direction instead of blending unrelated styles.
4. Implement real working code, not mockup-only markup.
5. Encode repeatable visual decisions as tokens, variables, or reusable classes/components.

## Core Rules

- Prefer a strong, coherent design direction over safe but generic UI.
- Follow this skill for typography, color behavior, spacing, geometry, and interaction details.
- Use precise layout, type, and motion choices; avoid decorative noise that does not support the concept.
- Keep accessibility intact while matching the intended visual system.
- Match implementation complexity to the design ambition: bold interfaces can justify richer code, while restrained interfaces need precision and restraint.
- Avoid overused AI-looking choices such as generic fonts, default component-library composition, and context-free gradients.
- If the user's request conflicts with this skill, follow the user's request and treat this skill as secondary guidance.

## Visual Theme

This project uses a Figma-inspired design language:

- Interface chrome is strictly monochrome: black and white only.
- Color lives in hero sections, product showcases, gradients, and embedded visual content.
- Typography carries most of the hierarchy through precise weight and tracking choices.
- Geometry leans on pills and circles instead of sharp-corner button shapes.
- Focus states should feel deliberate, especially dashed outlines that echo design-tool selection behavior.

Use the interface like a gallery wall: restrained chrome, expressive content.

## Color System

### Primary Colors

- Pure Black: `#000000`
- Pure White: `#ffffff`

Use these two colors for almost all interface chrome, text, borders, and buttons.

### Surface Treatments

- Glass Dark: `rgba(0, 0, 0, 0.08)`
- Glass Light: `rgba(255, 255, 255, 0.16)`

Use glass treatments sparingly for secondary actions or controls on contrasting surfaces.

### Gradient Behavior

- Hero gradients should feel vibrant and product-like, often using electric green, bright yellow, deep purple, and hot pink.
- Do not spread those colors into general UI chrome.
- If a section needs strong chroma, confine it to content zones, not the global shell.

## Typography

### Font Families

- Primary: `figmaSans`, fallback to `figmaSans Fallback, SF Pro Display, system-ui, helvetica`
- Mono / Label: `figmaMono`, fallback to `figmaMono Fallback, SF Mono, menlo`

### Typography Principles

- Prefer variable font precision over generic regular/medium/bold jumps.
- Use unusual weight stops where available: `320, 330, 340, 450, 480, 540, 700`.
- Body text should often sit in the lighter range rather than defaulting to `400`.
- Enable kerning globally where possible.
- Use negative letter-spacing by default for non-mono text.
- Use uppercase mono labels with positive letter-spacing for structural cues.

### Suggested Scale

| Role | Font | Size | Weight | Line Height | Letter Spacing |
|------|------|------|--------|-------------|----------------|
| Display / Hero | figmaSans | 86px | 400 | 1.00 | -1.72px |
| Section Heading | figmaSans | 64px | 400 | 1.10 | -0.96px |
| Sub-heading | figmaSans | 26px | 540 | 1.35 | -0.26px |
| Sub-heading Light | figmaSans | 26px | 340 | 1.35 | -0.26px |
| Feature Title | figmaSans | 24px | 700 | 1.45 | normal |
| Body Large | figmaSans | 20px | 330-450 | 1.30-1.40 | -0.10px to -0.14px |
| Body / Button | figmaSans | 16px | 330-400 | 1.40-1.45 | -0.14px to normal |
| Body Light | figmaSans | 18px | 320 | 1.45 | -0.26px to normal |
| Mono Label | figmaMono | 18px | 400 | 1.30 | 0.54px |
| Mono Small | figmaMono | 12px | 400 | 1.00 | 0.60px |

## Geometry And Components

### Radius Scale

- Minimal: `2px`
- Subtle: `6px`
- Comfortable: `8px`
- Pill: `50px`
- Circle: `50%`

### Buttons

Use these defaults unless the task requires a justified exception:

- Black Solid Pill: black background, white text, pill or circular geometry, dashed focus
- White Pill: white background, black text, pill geometry, dashed focus
- Glass Dark: subtle black overlay, black text, circular geometry, dashed focus
- Glass Light: subtle white overlay, white text, circular geometry, dashed focus

### Focus States

- Prefer `dashed 2px` outlines on interactive elements.
- Focus styling should feel signature, not browser-default.
- Keep focus states accessible and visible on both monochrome and gradient surfaces.

### Cards And Containers

- Use white surfaces for cards placed on colorful or dark backgrounds.
- Keep borders minimal.
- Use `6px` to `8px` radius for containers, cards, images, and dialogs.
- Shadows should be subtle; depth comes more from contrast and composition than heavy elevation.

### Navigation

- Clean horizontal nav on white.
- Tabs and segmented controls should use pill geometry.
- Standard links can use black text with understated underline treatment.
- Primary CTA should usually be a black pill button.

## Layout Principles

### Spacing

- Base unit: `8px`
- Common values: `1px, 2px, 4px, 4.5px, 8px, 10px, 12px, 16px, 18px, 24px, 32px, 40px, 46px, 48px, 50px`

### Composition

- Prefer gallery-like pacing with clear breathing room between major sections.
- Use full-width hero treatments when the content benefits from immersion.
- Let colorful sections act as visual relief between restrained monochrome areas.
- On wide screens, allow product content to feel expansive rather than boxed into narrow templates.

### Whitespace Philosophy

- Use generous whitespace to make content feel curated.
- If density is needed, keep it intentional and rhythmically structured.
- Avoid generic SaaS layouts with evenly spaced, interchangeable blocks.

## Depth And Elevation

- Flat: no shadow for page background and most text layers
- Surface: white cards on gradient or dark sections
- Elevated: subtle shadow for floating cards or hover states

Shadows are secondary. Contrast, color blocking, and the dimensionality of content should do most of the depth work.

## Responsive Behavior

### Breakpoints

- Small Mobile: `<560px`
- Tablet: `560-768px`
- Small Desktop: `768-960px`
- Desktop: `960-1280px`
- Large Desktop: `1280-1440px`
- Ultra-wide: `1440-1920px`

### Responsive Rules

- Scale hero text down aggressively: `86px -> 64px -> 48px`
- Let product tabs scroll horizontally on mobile if necessary
- Collapse multi-column content into clear stacked sections
- Preserve the visual hierarchy, not just the DOM order

## Do

- Use monochrome chrome and reserve color for expressive content zones
- Use pill and circular geometry for interactive elements
- Use precise variable font weights where available
- Apply negative tracking to body and display text where appropriate
- Use mono uppercase labels for technical or structural markers
- Make hover, focus, and motion states feel intentionally designed

## Don't

- Don't add random interface accent colors to the chrome
- Don't default to generic font stacks like Arial, Roboto, or Inter if the intended fonts are available
- Don't use sharp-corner buttons for primary controls
- Don't use solid generic focus outlines when dashed focus is part of the system
- Don't overuse heavy shadows, glass, or blur
- Don't build cookie-cutter layouts that could belong to any template

## Prompting Hints

When generating or refining UI, think in prompts like:

- "Create a hero on a vibrant multi-color gradient with white display text and a white pill CTA."
- "Build a product tab bar with pill-shaped buttons; active state black with white text."
- "Use mono uppercase labels with positive tracking for section markers."
- "Keep interface chrome black and white; color belongs to the product content, not the shell."

## Implementation Checklist

- Is the layout visually intentional and specific to the task?
- Are typography and spacing doing most of the design work?
- Are repeated values extracted into variables or reusable patterns?
- Do hover, focus, and motion states feel designed rather than default?
- Does the result avoid generic template aesthetics?

## Output Expectation

Produce frontend code that is:

- Production-grade and functional
- Visually cohesive
- Faithful to this visual system where applicable
- Refined enough that another pass is for polish, not basic cleanup
