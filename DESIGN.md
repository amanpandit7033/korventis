# Design System Strategy: High-End Tech Editorial

## 1. Overview & Creative North Star: "The Architectural Authority"
This design system rejects the "template-ready" corporate look in favor of **Architectural Authority**. We are moving away from the cluttered, line-heavy interfaces of legacy tech firms toward a high-end editorial experience. 

The North Star is defined by **Intentional Asymmetry** and **Tonal Depth**. Instead of standard grids, we use expansive white space and large-scale typography to create a sense of scale and confidence. We do not use borders to define space; we use light and shadow—specifically, the way light hits physical surfaces. Every element should feel like a custom-milled piece of hardware: solid, premium, and purposefully placed.

---

### 2. Colors: Tonal Layering over Line Work
The palette is rooted in the depth of `primary_container` (#002147) and the purity of `surface_container_lowest` (#ffffff). To maintain an elite aesthetic, we follow two non-negotiable rules:

*   **The "No-Line" Rule:** 1px solid borders are strictly prohibited for sectioning. Boundaries must be defined solely through background shifts. For example, a `surface_container_low` section sitting against a `surface` background provides all the separation a sophisticated eye needs.
*   **Surface Hierarchy & Nesting:** Treat the UI as stacked sheets of fine paper. 
    *   **Base:** `background` (#f7f9fb)
    *   **Sections:** `surface_container_low` (#f2f4f6)
    *   **Interactive Cards:** `surface_container_lowest` (#ffffff)
*   **The "Glass & Gradient" Rule:** Main CTAs should not be flat. Use a subtle linear gradient from `secondary` (#0054cd) to `secondary_container` (#316ee9) at a 135-degree angle. Floating navigation elements should utilize a `surface_container_lowest` color at 80% opacity with a `20px` backdrop-blur to create an integrated, high-tech glass effect.

---

### 3. Typography: Editorial Sophistication
We pair the geometric precision of **Manrope** for high-impact displays with the functional clarity of **Inter** for utility.

*   **Display & Headline (Manrope):** These are your "Brand Moments." Use `display-lg` (3.5rem) with tighter letter-spacing (-0.02em) to convey power. Headlines should dominate the white space, often pushed to the far left or right to break traditional symmetry.
*   **Body & Label (Inter):** Reserved for technical data and narrative. `body-lg` (1rem) is the standard for service descriptions. 
*   **Tonal Contrast:** Never use pure black for text. Use `on_surface_variant` (#44474e) for secondary body copy to reduce visual noise and maintain the "Slate Grey" editorial feel requested by the brand.

---

### 4. Elevation & Depth: The Physics of UI
Hierarchy is achieved through **Tonal Layering**, not structural scaffolding.

*   **The Layering Principle:** To lift a card, do not reach for a shadow first. Place a `surface_container_lowest` card on a `surface_container_high` background. The natural contrast creates a "soft lift."
*   **Ambient Shadows:** If an element must float (e.g., a dropdown or a primary modal), use an "Ambient Shadow": 
    *   `box-shadow: 0 24px 48px -12px rgba(0, 33, 71, 0.08);` 
    *   Note the use of the Navy Blue (`primary_container`) in the shadow color rather than grey. This makes the shadow feel like a natural reflection of the brand's core color.
*   **The "Ghost Border" Fallback:** If accessibility requires a container edge (e.g., in high-contrast modes), use `outline_variant` (#c4c6cf) at **15% opacity**. It should be felt, not seen.

---

### 5. Components

#### Buttons & CTAs
*   **Action Primary:** Uses the signature gradient (Action Blue). `rounded-lg` (0.5rem). Text is `on_primary` (#ffffff), bolded, using `label-md`.
*   **Secondary/Ghost:** No background. `outline` color at 20% opacity for the "Ghost Border," or simply a text-link with a custom `2px` underline offset.

#### Service Cards & Portfolio Grids
*   **Structure:** No dividers. Use `Spacing-8` (2.75rem) to separate the image from the text. 
*   **Interaction:** On hover, the card should transition from `surface_container_low` to `surface_container_lowest` with an Ambient Shadow.
*   **Portfolio:** Use an asymmetrical masonry grid rather than a standard 3x3. Large-scale projects should span 2 columns to disrupt the "template" feel.

#### Professional Forms
*   **Input Fields:** `surface_container_lowest` background. No border. Instead, use a `2px` bottom-bar in `outline_variant`. On focus, the bottom-bar transitions to `secondary` (Action Blue).
*   **Validation:** Error states use `error` (#ba1a1a) but maintain the soft styling—use a `surface_container_high` background with red text for error messages to keep the palette sophisticated.

#### Additional Component: The "Contextual Breadcrumb"
*   For a tech services company, path-finding is key. Use `label-sm` in all caps with `Spacing-1.5` tracking. This acts as a "metadata" header above main headlines to provide an elite, curated feel.

---

### 6. Do’s and Don'ts

*   **DO:** Use the full `Spacing Scale`. If a section feels crowded, double the padding. High-end design lives in the "breathing room."
*   **DO:** Mix typography weights. A `display-md` in Bold paired with a `body-lg` in Regular creates an authoritative hierarchy.
*   **DON'T:** Use 100% opaque lines to separate content. This is the fastest way to make the design look like a generic corporate portal.
*   **DON'T:** Use standard "Drop Shadows." If the shadow looks like a fuzzy grey line, it’s too heavy. It should look like an atmospheric glow.
*   **DO:** Ensure `secondary` (Action Blue) is used sparingly. It is a laser-pointer, not a paint bucket. Use it only where you want the user to click.