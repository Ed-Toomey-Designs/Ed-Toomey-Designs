# Design System: Editorial Industrialism

## 1. Overview & Creative North Star
**Creative North Star: The Precision Workshop**
This design system moves away from the "template" aesthetic of standard fabrication sites and leans into the world of high-end editorial archives. It is inspired by the meticulous blueprint of an architect and the raw, polished finish of a master metalworker.

We achieve this through **Editorial Industrialism**: a philosophy where whitespace is as structural as steel. We break the rigid, centered grid by utilizing intentional asymmetry—placing oversized typography against tight, technical labels. By overlapping high-resolution imagery with semi-transparent surfaces, we create a sense of depth and tactile "soul" that reflects the custom, hand-crafted nature of the business.

---

### 2. Colors
The palette is a sophisticated blend of raw materials (Steel and Slate) juxtaposed against a warm, metallic "Copper" primary accent.

*   **Primary (Copper):** `#874d30` (Primary) / `#a46546` (Container). Use these to draw the eye to craftsmanship and action.
*   **Neutral (Slate & Steel):** `#515f74` (Secondary) and `#191c1e` (On Surface). These provide the industrial weight.
*   **Foundation:** `#f7f9fb` (Surface/Background). A crisp, cool-white canvas.

**The "No-Line" Rule**
Never use a 1px solid border to separate sections. Structure must be defined by tonal shifts. For example, a hero section on `surface` transitions into a service listing on `surface-container-low`. The absence of lines forces the user’s eye to follow the natural flow of the material layers.

**Surface Hierarchy & Nesting**
Treat the UI as a physical assembly.
*   **Base:** `surface` (#f7f9fb)
*   **Sectioning:** `surface-container-low` (#f2f4f6)
*   **Elevated Components:** `surface-container-lowest` (#ffffff) for cards to make them feel like "floating" sheets of paper on a steel workbench.

**The Glass & Gradient Rule**
To mimic the reflection of brushed metal, use Glassmorphism for floating navigation bars or image overlays. Utilize `surface` colors at 80% opacity with a `20px` backdrop blur. Use a subtle linear gradient from `primary` to `primary_container` for CTAs to create a metallic sheen rather than a flat "plastic" button.

---

### 3. Typography
The type system balances the technical rigidity of `Space Grotesk` with the human, storytelling quality of `Newsreader`.

*   **Display & Headlines (Space Grotesk):** Modern, wide-set, and authoritative. Use `display-lg` for project titles to create a "blueprint" feel.
*   **Body (Newsreader):** A sophisticated serif that suggests heritage and bespoke quality. Use `body-lg` for service descriptions to ensure high-end readability.
*   **Labels (Inter):** Small, all-caps, and mono-spaced in feel. Use `label-md` for technical specs, dimensions, or fabrication dates.

---

### 4. Elevation & Depth
In an industrial context, depth is created by stacking materials, not by artificial lighting.

*   **The Layering Principle:** Rather than shadows, use `surface-container-highest` (#e0e3e5) to define a "recessed" area for technical data, and `surface-container-lowest` (#ffffff) for "active" or "raised" elements.
*   **Ambient Shadows:** For floating elements (e.g., a quote request modal), use an ultra-diffused shadow: `box-shadow: 0 20px 40px rgba(25, 28, 30, 0.06);`. The shadow must feel like ambient light hitting a heavy object.
*   **The Ghost Border:** If a boundary is required (e.g., an input field), use `outline-variant` (#d8c2b9) at 20% opacity. It should be felt, not seen.

---

### 5. Components

**Buttons (The Forged Action)**
*   **Primary:** Gradient from `primary` to `primary_container`. No border. `0.25rem` (sm) radius for a sharp, precision-cut look.
*   **Secondary:** `surface-container-highest` background with `on-surface` text. 
*   **Tertiary:** Text-only, using `label-md` styling with a copper underline that expands on hover.

**Portfolio Gallery (The Blueprint Grid)**
*   Forbid dividers. Use `2rem` gaps.
*   Use asymmetrical layouts: one large "Hero" project image spanning 2/3 of the width, with technical metadata (Material, Process, Year) in `label-sm` tucked into the 1/3 white space.

**Cards (Service & Fabrication)**
*   No borders or heavy shadows.
*   Use `surface-container-low` for the card background. 
*   On hover, transition the background to `surface-container-lowest` and apply a `primary` (Copper) accent line (2px) at the very top of the card.

**Input Fields (Quote Requests)**
*   Background: `surface-container-highest`.
*   Border: None, except for a bottom "Ghost Border" that transforms into a `primary` color line on focus.
*   Label: `label-sm` placed above the field, never inside.

---

### 6. Do's and Don'ts

**Do:**
*   **Do** use extreme whitespace. Let the "industrial" elements breathe like a gallery space.
*   **Do** use `Space Grotesk` in all-caps for metadata and headers.
*   **Do** overlap elements. Let an image slightly bleed into the next `surface-container` to create a cohesive, custom-built feel.

**Don't:**
*   **Don't** use standard `0.5rem` rounded corners. Use `0.25rem` (sm) or `none` to maintain a sharp, fabricated edge.
*   **Don't** use pure black `#000000`. Use `on-surface` (#191c1e) for a softer, more premium "ink on paper" or "anodized steel" look.
*   **Don't** use icons that are too playful or rounded. Use thin-stroke, geometric, or technical-style iconography.