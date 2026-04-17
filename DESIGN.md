# Design System Document: The Sovereign Editorial

## 1. Overview & Creative North Star
**Creative North Star: The Sovereign Editorial**

This design system moves away from the "template-heavy" world of corporate law and into the realm of high-end editorial prestige. The objective is to convey an unwavering sense of authority and quiet confidence. We achieve this by breaking the rigid, boxed-in grids common in legal tech and replacing them with **intentional asymmetry, expansive white space, and layered tonal depth.**

The UI should feel like a curated publication—think *The Financial Times* meets a private gallery. We use overlapping elements, sophisticated serif type scales, and a "No-Line" philosophy to create a digital environment that feels architecturally sound yet fluid and modern.

---

## 2. Colors & Surface Philosophy
Our palette is rooted in heritage: deep oceanic navies, charcoal silts, and the warmth of burnished gold.

### The "No-Line" Rule
**Explicit Instruction:** You are prohibited from using 1px solid borders to define sections. Layout boundaries must be established exclusively through background color shifts. For example, a `surface-container-low` section should sit against a `surface` background to define its start and end. 

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers, like heavy cardstock stacked on a mahogany desk. 
*   **Base:** `surface` (#fbf9fa) is your canvas.
*   **Sections:** Use `surface-container-low` (#f5f3f4) for secondary content areas.
*   **Prominent Cards:** Use `surface-container-lowest` (#ffffff) to create a "lifted" effect through color contrast, not lines.
*   **Interactive Overlays:** Use `surface-container-highest` (#e4e2e3) for elements that require immediate attention.

### The "Glass & Gradient" Rule
To add "soul" to the navy tones, avoid flat hex fills for large areas. 
*   **Hero Sections:** Apply a subtle radial gradient transitioning from `primary` (#041627) to `primary_container` (#1a2b3c). 
*   **Glassmorphism:** For floating navigation bars or context menus, use the `surface` color at 85% opacity with a `20px backdrop-blur`. This ensures the brand’s sophisticated textures bleed through the UI layers.

---

## 3. Typography
The typographic soul of this system is the tension between the historic authority of the serif and the modern precision of the sans-serif.

*   **The Statement (Display & Headlines):** Use **Noto Serif**. This is our "Editorial Voice." It should be used for high-impact statements, practice area titles, and partner names. Use `display-lg` (3.5rem) with tighter letter-spacing (-0.02em) to create an authoritative, "printed" feel.
*   **The Evidence (Body & Titles):** Use **Manrope**. This sans-serif is clean, geometric, and highly legible. Use it for case descriptions, legal insights, and functional UI elements.
*   **The Footnote (Labels):** Use `label-md` (0.75rem) in all-caps with increased letter-spacing (0.05em) for category tags or dates to mimic the precision of legal documents.

---

## 4. Elevation & Depth
We eschew the "material" look for a more organic, ambient sense of depth.

*   **Tonal Layering:** Hierarchy is achieved by "stacking." A `surface-container-lowest` card placed atop a `surface-container-low` background creates a natural, soft lift.
*   **Ambient Shadows:** When a float is required (e.g., a primary CTA or a dropdown), use ultra-diffused shadows. 
    *   *Value:* `0px 24px 48px rgba(27, 28, 29, 0.06)`. 
    *   Shadows should never be grey; they should be a low-opacity tint of `on_surface`.
*   **The Ghost Border:** If a boundary is strictly required for accessibility, use a "Ghost Border": the `outline_variant` token at **15% opacity**. This creates a suggestion of a container without disrupting the editorial flow.

---

## 5. Components

### Buttons
*   **Primary:** Solid `tertiary_fixed_dim` (#e9c176) with `on_tertiary_fixed` text. Sharp `DEFAULT` (0.25rem) corners. No gradients.
*   **Secondary:** Ghost style. No background, `outline` token at 20% for the border, and `notoSerif` for the text to signify importance.
*   **Tertiary:** Text only, Manrope Bold, with a 1px underline that expands on hover.

### Cards & Lists
*   **The Card Rule:** No borders, no dividers. Separate list items using the `Spacing Scale` (suggested: 24px or 32px vertical gaps). 
*   **Interactive Cards:** On hover, a card should shift from `surface` to `surface-container-high`. The transition must be slow (300ms) to feel "heavy" and prestigious.

### Input Fields
*   **Styling:** Use the "Ghost Border" approach. A bottom-only border using `outline_variant` is preferred for a minimalist, "fill-in-the-blank" legal document aesthetic.
*   **Focus State:** The border transitions to `primary` (#041627) with a subtle 2px thickness.

### Signature Components
*   **The "Statute" Pull-quote:** A large `notoSerif` quote mark in `tertiary_fixed_dim` (#e9c176) at 10% opacity, layered behind `headline-md` text.
*   **The Partner Spotlight:** An asymmetrical layout where the profile image (high-contrast, professional) overlaps a `primary_container` decorative block.

---

## 6. Do's and Don'ts

### Do:
*   **Embrace Asymmetry:** Align text to the left but allow imagery to bleed off the right edge of the grid.
*   **Use Texture:** Subtle paper grain or marble textures should be applied to `surface-container` backgrounds at very low opacity (3-5%).
*   **Master the White Space:** If you think there is enough padding, add 16px more. Prestige requires room to breathe.

### Don't:
*   **Don't use 100% Black:** Always use `on_background` (#1b1c1d) or `primary` (#041627) for text. Pure black feels "cheap" and unrefined.
*   **Don't use Rounded Pills:** Stick to `DEFAULT` (4px) or `sm` (2px) corner radii. Large rounded corners feel too "tech-startup" for a prestigious firm.
*   **Don't use Standard Icons:** Avoid "bubbly" icon sets. Use thin-stroke, sharp-cornered icons (0.75px to 1px stroke weight).

---
*Director's Final Note: Every pixel should feel like a conscious decision. If an element doesn't serve the narrative of "Authority" or "Trust," remove it. We are not building a website; we are building a digital legacy.*