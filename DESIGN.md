# Design System Strategy: Cinematic Immersion

## 1. Overview & Creative North Star

### Creative North Star: "The Digital Auteur"
This design system is not a utility; it is a stage. Moving away from the "boxed-in" layout of traditional SaaS or corporate sites, "The Digital Auteur" treats the browser as a cinematic lens. We achieve this through **intentional asymmetry**, **maximalist typography scales**, and **tonal depth**.

The experience is defined by high-contrast transitions and a moderate level of whitespace that mimics the "breathing room" of a premium gallery. By overlapping large-scale typography with immersive media and utilizing "nested" surface logic, we break the grid to create a narrative flow that feels professional yet creatively uninhibited.

---

## 2. Colors

### Palette Logic
The color system is anchored in `neutral_color_hex` (#0D0D0D), providing a true dark-mode canvas that allows our high-chroma accents to vibrate. 
- **Primary (`primary_color_hex`: #daaa00):** A warm Golden Yellow used for high-level branding and primary CTAs.
- **Secondary (`secondary_color_hex`: #71b2c9):** A sophisticated Steel Teal designed to cut through the darkness, used for interaction cues and success states.
- **Tertiary (`tertiary_color_hex`: #ffffff):** Clean White for subtle differentiation, highlights, and contrast in complex layouts.
- **Logo:** "GLOBAL EVENTS" wordmark is always rendered in solid `#ffffff`.

### The "No-Line" Rule
**Explicit Instruction:** 1px solid borders are strictly prohibited for sectioning or card definition. Structural boundaries must be defined solely through background color shifts. For example, a `surface-container-low` card sitting on a `surface` background creates a sophisticated, borderless edge that feels modern and integrated.

### Surface Hierarchy & Nesting
Treat the UI as physical layers of smoked glass. 
- Use `surface-container-lowest` (#0e0e0e) for the deep background.
- Use `surface-container-high` (#2a2a2a) or `surface-bright` (#3a3939) for elevated elements.
- This creates "nested depth" where components feel like they are emerging from the shadows rather than being pasted on top.

### Signature Textures
To avoid a flat "template" look, use a subtle linear gradient on main CTAs and Hero headers:
- **Primary Gradient:** Transition from `primary` (#daaa00) to `tertiary` (#ffffff) at a 135-degree angle. This adds a "soul" to the color that flat hex codes cannot replicate.

---

## 3. Typography

The typographic system is a dialogue between the industrial strength of **Epilogue** and the human clarity of **Manrope**.

- **Display & Headlines (Epilogue):** These are the "shouting" elements. High-impact, bold, and unapologetic. Use `display-lg` (3.5rem) with tight letter-spacing to command attention in Hero sections.
- **Body & Titles (Manrope):** Chosen for its clean, geometric legibility. Use `body-lg` for editorial copy and `title-lg` for section headers.
- **Hierarchy as Identity:** The massive scale contrast between `display-lg` and `body-sm` is intentional. It conveys an authoritative, "editorial" brand voice—moving the site from a "webpage" to a "publication."

---

## 4. Elevation & Depth

### The Layering Principle
Depth is achieved through **Tonal Layering**. Place a `surface-container-highest` card inside a `surface-container-low` section. The contrast in value provides all the "lift" required.

### Ambient Shadows
If a floating effect is required (e.g., a modal or floating navigation), use "Ambient Shadows":
- **Blur:** 40px - 60px.
- **Opacity:** 6% - 10%.
- **Color:** Use a tinted version of `on_surface` (a deep, desaturated purple-grey) rather than black. This mimics natural light diffusion.

### Glassmorphism
Floating elements should leverage `backdrop-blur` (12px to 20px) combined with a semi-transparent `surface_variant` (#353534 at 60% opacity). This allows the vibrant event photography to bleed through the UI, maintaining the cinematic immersion.

---

## 5. Components

### Buttons
- **Primary:** Filled with the Primary Gradient. `Roundedness: 1` (subtle roundedness). Text: `label-md` uppercase, bold.
- **Secondary:** Ghost style. No background, but use a "Ghost Border" (20% opacity `outline_variant`).
- **Interaction:** On hover, primary buttons should exhibit a subtle glow (Box-shadow using `secondary` (#71b2c9) at 15% opacity).

### Cards & Lists
- **Prohibition:** Do not use divider lines.
- **Separation:** Content must be separated by the Spacing Scale (normal whitespace) or a tonal shift from `surface` to `surface_container`.
- **Media Cards:** Aspect ratio 16:9 or 4:5. Text should overlap the image using a `surface_container_lowest` scrim (gradient overlay) for legibility.

### Chips & Tags
- Use `full` roundedness (pill shape). 
- Background: `surface_container_high`. Text: `secondary` (#71b2c9).

### Input Fields
- **State:** Unfocused inputs use `surface_container_highest` with no border. 
- **Focus State:** Transition to a 1px "Ghost Border" using the `secondary` (#71b2c9) Teal at 50% opacity.

---

## 6. Do's and Don'ts

### Do:
- **Use Intentional Asymmetry:** Offset images and text blocks. Let a headline hang over the edge of a container.
- **Embrace the Dark:** Use the `surface-container-lowest` (#0e0e0e) for the footer to "ground" the page.
- **Leverage High Contrast:** Ensure `secondary` (#71b2c9) Teal is used for the most critical user actions to guide the eye instantly.

### Don't:
- **Don't use 100% Opaque Borders:** This creates a "cheap" grid-like feel that destroys the cinematic atmosphere.
- **Don't Crowd the Content:** If a section feels full, add 40px of extra padding. Whitespace in this system is a luxury, not a void.
- **Don't use Standard Drop Shadows:** Avoid the "fuzzy black" shadow. If it doesn't look like ambient light, remove it.
- **Don't use Center-Alignment for Everything:** Keep the layout dynamic. Center alignment should be reserved for the Hero or "The End" CTA only.