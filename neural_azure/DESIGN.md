# Design System Document: The High-End Editorial Portfolio

## 1. Overview & Creative North Star: "The Neural Architect"
This design system is built to position an AI/ML student not just as a coder, but as an architect of intelligence. We are moving away from the "generic tech portfolio" template and toward a high-end, editorial experience that mirrors the precision of machine learning and the fluidity of neural networks.

**The Creative North Star: The Neural Architect.**
This system celebrates "Intelligent Depth." It breaks the traditional rigid grid through intentional asymmetry, overlapping elements, and high-contrast typography scales. The layout should feel like a premium digital gallery—spacious, authoritative, and sophisticated. We achieve this by prioritizing breathing room (negative space) and utilizing glassmorphism to suggest the "transparency" and "layers" of complex AI models.

---

## 2. Colors
The color palette is anchored in a deep, nocturnal base (`#111417`) to allow the vibrant, electric blues to feel like glowing data points in a void.

### The "No-Line" Rule
**Explicit Instruction:** You are prohibited from using 1px solid borders to define sections. Traditional dividers are a sign of "template" design. Boundaries must be defined solely through:
1.  **Background Color Shifts:** Transitioning from `surface` to `surface_container_low`.
2.  **Tonal Transitions:** Using subtle gradients to suggest the end of one thought and the beginning of another.

### Surface Hierarchy & Nesting
Instead of a flat grid, treat the UI as a series of stacked, physical layers. 
- **The Base:** Use `surface` (`#111417`) for the main page background.
- **The Section:** Use `surface_container_low` (`#191c1f`) for large content blocks (e.g., the "Experience" section).
- **The Component:** Use `surface_container_high` (`#282a2e`) for cards sitting inside those sections.
This "nesting" creates natural depth without visual clutter.

### The "Glass & Gradient" Rule
To inject "soul" into the professional interface:
- **Glassmorphism:** Floating elements like the Sticky Navbar must use a semi-transparent `surface_container` with a `backdrop-filter: blur(20px)`. 
- **Signature Textures:** For primary CTAs and Hero accents, use a linear gradient: `primary_container` (`#2d5bff`) to `primary` (`#b8c3ff`) at a 135-degree angle. This provides a professional polish that flat hex codes cannot achieve.

---

## 3. Typography
The typography strategy is a dialogue between the technical precision of **Inter** and the modern, wide-aperture authority of **Manrope**.

- **Display & Headline (Manrope):** Used for "Brand Moments." These should be set with tight letter-spacing (-2%) to feel impactful and "intelligent." Use `display-lg` for hero statements to command immediate attention.
- **Titles & Body (Inter):** Used for "Information Delivery." Inter’s neutrality ensures that complex project descriptions remain legible.
- **Label & Small (Inter):** Used for "Metadata." Set these in `label-md` or `label-sm` with slightly increased letter-spacing (+5%) and Uppercase styling for a technical, "coded" feel.

---

## 4. Elevation & Depth
In this system, we do not use "shadows" in the traditional sense; we use **Ambient Glows and Tonal Layering.**

- **The Layering Principle:** Depth is achieved by stacking the surface-container tiers. Placing a `surface_container_highest` element onto a `surface_dim` background creates a soft, natural lift.
- **Ambient Shadows:** When a card requires a "floating" effect (e.g., on hover), use an extra-diffused shadow:
    - *Blur:* 40px
    - *Spread:* -10px
    - *Color:* A 10% opacity version of `inverse_primary` (`#104af0`). This creates a subtle blue "aura" rather than a grey "drop shadow."
- **The "Ghost Border" Fallback:** If a container absolutely requires definition against a similar background, use a **Ghost Border**: `outline_variant` (`#434656`) at **15% opacity**. Never 100%.

---

## 5. Components

### Buttons
- **Primary:** Rounded (`xl`: 1.5rem), using the signature gradient. Text is `on_primary_container`. On hover, increase the gradient intensity.
- **Secondary:** Transparent background with a "Ghost Border" and `primary` text.
- **Tertiary:** No background or border. Text only with a `primary` underline that expands from center on hover.

### Cards & Project Tiles
- **Construction:** Use `surface_container_high` with a `lg` (1rem) roundedness.
- **Restriction:** **Strictly no dividers.** Separate header, body, and footer content using the vertical spacing scale (e.g., 24px gaps).
- **Interaction:** On hover, the card should lift slightly (translateY -4px) and the Ghost Border should increase in opacity from 15% to 40%.

### Chips (Skills/Tags)
- **Selection Chips:** Use `secondary_container` with `on_secondary_container` text. Roundedness should be `full`.
- **Styling:** Keep these small (`label-md`) to ensure they don't distract from the primary content.

### Sticky Navbar
- **Styling:** `surface_container_lowest` at 70% opacity. 
- **Blur:** 12px backdrop-blur. 
- **Layout:** Use an asymmetrical layout—logo on the far left, navigation links grouped tightly on the right to create "tension" and interest.

### Input Fields (Contact Form)
- **Style:** Minimalist. Only a bottom border using `outline_variant` at 40%. 
- **Active State:** The bottom border transforms into a 2px `primary` line. Labels should use `label-md` and float above the field.

---

## 6. Do's and Don'ts

### Do:
- **Do use intentional asymmetry.** If a project description is on the left, let the image bleed off the right edge of the grid.
- **Do use "Breathable" Spacing.** When in doubt, add more padding. The "Neural Architect" does not feel cramped.
- **Do use high-contrast type scales.** A massive `display-lg` headline next to a tiny, sophisticated `label-sm` metadata tag creates an editorial feel.

### Don't:
- **Don't use pure black (#000000).** It kills the depth. Always use the `surface` tokens.
- **Don't use standard icons.** Use thin-stroke (Light or Thin weight) SVG icons to match the sophistication of the Manrope typeface.
- **Don't use 100% opaque borders.** They act as "visual speedbumps" and break the fluid, glass-like flow of the system.
- **Don't use default "Blue."** Only use the specific `primary` and `primary_container` tokens provided to maintain the "Vibrant Blue" brand identity.