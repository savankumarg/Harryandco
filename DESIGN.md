# Design System: L’Excellence Visual Language

## 1. Overview & Creative North Star
**Creative North Star: "The Digital Atelier"**

This design system is not a template; it is a curated editorial experience. It moves away from the rigid, boxed-in structures of traditional e-commerce to embrace the fluid, breathing space of a high-end physical boutique. By utilizing intentional asymmetry, overlapping elements, and extreme typographic contrast, we evoke the feeling of a bespoke gallery. 

The "Digital Atelier" philosophy dictates that every pixel must feel intentional. We avoid "standard" UI patterns in favor of cinematic layouts where the jewelry is the protagonist, and the interface acts as the soft, ambient light illuminating it.

## 2. Colors: Tonal Depth & Soul
The palette is rooted in the interplay between shadow and light. We utilize a monochromatic base of Deep Black and Pure White, punctuated by the warmth of Gold.

### The "No-Line" Rule
**Borders are prohibited for sectioning.** To define the transition between content areas, use shifts in the surface hierarchy (e.g., a section in `surface_container_low` transitioning into `surface_container_lowest`). Boundaries are felt, not seen.

### Surface Hierarchy & Nesting
Instead of a flat grid, treat the UI as layered sheets of obsidian and frosted glass.
- **Base Layer:** `surface` (#131313).
- **Secondary Depth:** `surface_container_low` for subtle background shifts.
- **Focus Containers:** Use `surface_container_highest` (#353534) for cards to create a "lifted" feel against the dark background.
- **Glassmorphism:** For floating navigation or modal overlays, use `surface` with 60% opacity and a `24px` backdrop-blur. This creates a "frosted" effect that allows the jewelry’s luster to bleed through the interface.

### Signature Textures
Main CTAs and Hero accents must use a subtle gradient: 
*   **The Golden Aura:** A linear gradient from `primary` (#f2ca50) to `primary_container` (#d4af37) at a 135-degree angle. This adds a metallic "shimmer" that flat colors cannot replicate.

## 3. Typography: Editorial Authority
We use a high-contrast pairing to balance heritage with modernity.

*   **Display & Headlines (Noto Serif / Playfair Display):** These are the "voice" of the brand. Use `display-lg` for hero statements. Tighten the letter-spacing (-0.02em) to create an authoritative, editorial feel. 
*   **Body & Titles (Manrope / Poppins):** Used for functional clarity. While the headings are romantic and expressive, the body text is utilitarian and clean. 
*   **The Scale:**
    *   **Display Large (3.5rem):** Reserved for hero titles and collection names.
    *   **Headline Medium (1.75rem):** For section headers and product names.
    *   **Body Medium (0.875rem):** For descriptions. Ensure line-height is generous (1.6) to maintain the "spacious" feel.
    *   **Label Small (0.6875rem):** All-caps with +0.1em tracking, used for metadata or "Exclusive" tags.

## 4. Elevation & Depth
In this design system, depth is a product of light and layering, not structural lines.

*   **The Layering Principle:** Place `surface_container_highest` elements atop `surface_dim` to create natural prominence. 
*   **Ambient Shadows:** For "floating" elements like product hover states, use a shadow with a 40px blur, 0px offset, and 6% opacity of the `on_surface` color. It should feel like an atmospheric glow, not a drop shadow.
*   **The "Ghost Border" Fallback:** If a boundary is strictly required for accessibility, use `outline_variant` (#4d4635) at 15% opacity. This creates a "whisper" of a line that defines space without cluttering the visual field.

## 5. Components: Minimalist Primitives

### Buttons
*   **Primary:** Uses the "Golden Aura" gradient. Rectangular with a `0.25rem` (DEFAULT) radius. No border. Text is `on_primary`.
*   **Secondary:** Ghost style. No background, `outline` border at 30% opacity. On hover, the background fills with a 5% `primary` tint.
*   **Tertiary:** Underlined text only (`title-sm`), using `primary`. The underline should be 1px and offset by 4px.

### Cards & Lists
*   **Rule:** Forbid divider lines.
*   **Implementation:** Separate items using `32px` or `48px` of vertical white space. For product grids, use asymmetrical sizing (e.g., a 2-column grid where one image is slightly larger than the other) to break the "template" feel.

### Input Fields
*   **Style:** Bottom-border only (`outline`, 1px). When focused, the border transitions to `primary` and the label slides up into a `label-sm` style.
*   **Error State:** Use `error` (#ffb4ab) only for the border and a small hint text; avoid large red blocks which break the luxury aesthetic.

### Boutique-Specific Components
*   **The "Lume" Carousel:** A product slider where the active item has a soft `primary_fixed` glow behind it, mimicking a spotlight in a dark boutique.
*   **Glass Drawer:** A side-navigation menu using 70% `surface_container_highest` with a heavy backdrop-blur (30px) for high-end filtering.

## 6. Do’s and Don'ts

### Do
*   **DO** use negative space aggressively. If a section feels crowded, double the padding.
*   **DO** overlap elements. Let a jewelry image slightly bleed over a headline to create a 3D, layered effect.
*   **DO** use imagery with "Chiaroscuro" lighting (high contrast between light and dark) to match the UI.

### Don't
*   **DON'T** use 100% opaque borders or dividers.
*   **DON'T** use standard "Material" shadows. If the shadow is visible enough to be identified as a "shadow," it is too heavy.
*   **DON'T** use "Pure Black" (#000000) for text. Always use `on_surface` or `on_surface_variant` to maintain a softer, premium tonal range.
*   **DON'T** use rounded corners above `0.75rem` (xl). Sharp or subtly rounded edges feel more architectural and "couture."