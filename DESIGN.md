# Design System: Editorial Fluidity

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Digital Curator."** 

Moving away from the rigid, block-based structures of traditional web design, this system treats the browser viewport as a high-end fashion editorial. It is defined by "Editorial Fluidity"—a marriage between the structured discipline of a Swiss grid and the organic movement of a premium print magazine. We break the "template" look through intentional asymmetry, where large-scale imagery is permitted to bleed off-canvas or overlap text, creating a sense of depth and curated chaos. This is not just a website; it is a digital exhibition where whitespace is as much a design element as the content itself.

## 2. Colors
Our palette is rooted in a minimalist grayscale foundation, punctured by high-energy crimson to guide the eye to primary actions.

- **Primary & Neutrals:** We use `#1a1c1c` (On-Surface) for primary text to ensure readability, while the background stays at a crisp `#f9f9f9`.
- **The Crimson Pulse:** `secondary` (#ba0035) and `secondary_container` (#e21e49) are reserved exclusively for CTAs and interactive highlights. This creates a high-contrast focal point against the neutral backdrop.
- **The "No-Line" Rule:** To maintain the editorial feel, **1px solid borders are strictly prohibited for sectioning.** Boundaries between content blocks must be defined solely through background color shifts. For example, a `surface_container_low` section should sit flush against a `surface` background to define its territory.
- **Surface Hierarchy & Nesting:** Depth is created through tonal layering. Use `surface_container_lowest` (#ffffff) for elevated cards or floating elements and `surface_container_high` (#e8e8e8) for recessed or secondary content areas.
- **Signature Textures:** For high-impact areas like the Hero section, use subtle gradients transitioning from `primary` (#5b5b5b) to `primary_container` (#747474) to add a tactile, "ink-on-paper" depth that flat colors lack.

## 3. Typography
The typography system is a dialogue between the classic authority of the serif and the modern precision of the sans-serif.

- **Display & Headlines (Newsreader):** Our serif face is used for moments of "Voice." It conveys heritage and sophistication. The large scale of `display-lg` (3.5rem) should be used to anchor sections, often with tighter letter-spacing to feel like a magazine masthead.
- **Body & Labels (Manrope):** Our sans-serif face is the workhorse. It provides a clean, neutral contrast to the serif. Use `body-lg` for narrative descriptions and `label-md` for metadata or technical details.
- **Visual Hierarchy:** By pairing the organic curves of Newsreader with the geometric stability of Manrope, we establish a hierarchy that feels both authoritative and accessible.

## 4. Elevation & Depth
In this system, depth is a whisper, not a shout. We move away from heavy shadows in favor of "Tonal Layering."

- **The Layering Principle:** Stacking surfaces creates natural elevation. A `surface_container_lowest` (#ffffff) card placed on a `surface_container_low` (#f3f3f3) background provides all the separation required for a premium look.
- **Ambient Shadows:** When a floating effect is non-negotiable (e.g., a "sticky" contact button), use an ultra-diffused shadow. 
    - *Shadow Color:* A 4%–8% opacity version of `on_surface`.
    - *Blur:* 40px+. This mimics natural gallery lighting.
- **The "Ghost Border" Fallback:** If a container requires a border for accessibility (e.g., input fields), use the `outline_variant` token at 20% opacity. Never use 100% opaque borders.
- **Glassmorphism:** To integrate elements into the "Fluidity" theme, use `surface_bright` with a 70% opacity and a `backdrop-filter: blur(20px)`. This is especially effective for navigation bars and overlay modals, allowing the rich imagery to bleed through the UI.

## 5. Components

### Buttons
- **Primary:** High-contrast `on_secondary` text on a `secondary_container` (#e21e49) background. Use `full` roundedness for a pill shape that feels modern.
- **Secondary/Iconic:** A circular `secondary` button with a minimalist arrow icon. This acts as a "directional" prompt in the editorial layout.

### Cards & Projects
- **Image-First:** Cards should be borderless. Use a `lg` (0.5rem) corner radius for images to soften the grid.
- **Overlays:** Project titles should overlap image containers slightly using negative margins to break the "boxed" feel.
- **No Dividers:** Never use horizontal rules to separate list items. Use 48px–64px of vertical whitespace to denote a change in subject.

### Input Fields
- **Minimalist Frames:** Text inputs use a `surface_container_lowest` background with a 1px "Ghost Border." Focus states should transition the border to `secondary` (#ba0035).

### Signature Component: The "Fluid Accordion"
- Used for FAQs or Service lists. On hover, the background shifts from `surface` to `surface_container`. Instead of a standard chevron, use a numeric indicator in `secondary` color to emphasize the curated, list-like nature of the content.

## 6. Do's and Don'ts

### Do:
- **Use Large Margins:** Ensure the layout has at least 80px–120px of lateral whitespace on desktop to feel "high-end."
- **Embrace Asymmetry:** Offset images from their corresponding text blocks. Let the "white space" flow around elements like water.
- **Mix Media:** Combine high-fashion photography with minimalist typography to create a narrative.

### Don't:
- **Don't use 1px solid black borders:** It kills the "Fluid" editorial aesthetic and makes the site look like a wireframe.
- **Don't crowd the content:** If a section feels "busy," increase the `surface-container` spacing rather than adding lines or boxes.
- **Don't use standard drop shadows:** Avoid the "floating card" look common in SaaS dashboards. Our depth comes from color and blur, not heavy shadows.
- **Don't center-align everything:** Editorial layouts thrive on "anchored" alignments (e.g., a left-aligned heading paired with a right-aligned image).