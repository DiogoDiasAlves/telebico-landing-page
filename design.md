# Design System Document



## 1. Overview & Creative North Star: "The Modern Curator"

This design system is built to transcend the standard service provider template. Our Creative North Star is **"The Modern Curator"**—a philosophy that treats digital interfaces with the same intentionality as a high-end editorial lookbook.



We break the "generic grid" through the use of high-contrast structural elements, such as the signature dark, ultra-rounded navigation bar, and expansive, high-contrast typography. The visual identity relies on **intentional asymmetry** and **tonal depth** rather than decorative flourishes. By utilizing deep-radius corners (`xl: 3rem`) and a sophisticated interplay between vibrant action colors (`primary: #004ac6`) and soft, airy backgrounds (`surface: #faf8ff`), we create an environment that feels authoritative yet approachable.



---



## 2. Colors: Tonal Architecture

The palette is rooted in a "High-Contrast Clean" aesthetic. We use color to define boundaries and intent without relying on heavy UI baggage.



### The Color Logic

- **Primary & Action:** The `primary_container` (#2563eb) is our "Vibrant Blue." It is reserved for high-impact CTAs and core brand moments.

- **Surface Hierarchy:** We utilize the Material surface tokens to create a "nested" environment.

- **The "No-Line" Rule:** Explicitly prohibit the use of 1px solid borders for sectioning or containers. Boundaries must be defined through background shifts—for example, a `surface_container_low` section sitting on a `surface` background.

- **The "Glass & Gradient" Rule:** To elevate the premium feel, use Glassmorphism for floating UI elements (e.g., secondary navigation or info cards) using semi-transparent `surface_container_lowest` with a 12px–20px backdrop blur.

- **Signature Textures:** For Hero sections or primary buttons, use a subtle linear gradient transitioning from `primary` (#004ac6) to `primary_container` (#2563eb) at a 135-degree angle to add depth and "soul."



---



## 3. Typography: Editorial Authority

We use **Manrope** as our typographic backbone. It is a geometric sans-serif that balances modern tech aesthetics with humanist warmth.



* **Display (Large/Medium):** Reserved for Hero headlines. Use negative letter-spacing (-0.02em) to create a tight, editorial feel.

* *Display-LG: 3.5rem / Bold*

* **Headlines:** Used for section titles. High contrast against the body copy is essential.

* *Headline-MD: 1.75rem / Semi-Bold*

* **Body Text:** Prioritize legibility. Use `on_surface_variant` (#434655) for secondary body text to reduce visual noise while maintaining high readability.

* *Body-LG: 1rem / Regular*

* **Labels:** For overlines or small UI metadata, use `label-md` in all-caps with increased letter-spacing (+0.05em) for a sophisticated "caption" look.



---



## 4. Elevation & Depth: Tonal Layering

We reject traditional drop shadows in favor of **Ambient Light Mimicry**.



* **The Layering Principle:** Stacking tiers creates natural lift. Place a `surface_container_lowest` card on a `surface_container_low` section to define a container without a single line of CSS border.

* **Ambient Shadows:** When a floating element (like a primary button or a floating nav) requires a shadow, use an extra-diffused blur: `0px 20px 40px rgba(25, 27, 35, 0.06)`. The shadow must feel like air, not ink.

* **The "Ghost Border" Fallback:** If a container must be defined against a similar background, use a "Ghost Border": the `outline_variant` (#c3c6d7) at **15% opacity**. Never use a 100% opaque border.

* **Glassmorphism:** Navigation bars and "Book Now" widgets should use a frosted effect to allow hero imagery to bleed through, softening the transition between content and UI.



---



## 5. Components: Bespoke Service Patterns



### The Signature Navigation Bar

The header is a dark, pill-shaped floating element (`inverse_surface: #2e3039`) with a `full` (9999px) or `xl` (3rem) corner radius. It should sit detached from the top of the viewport with `spacing-4` margin to reinforce the "curated" look.



### Buttons

- **Primary:** High-contrast `primary_container` (#2563eb) with `on_primary` text. Radius: `full`. Padding: `spacing-3` (top/bottom) by `spacing-8` (left/right).

- **Secondary (The Editorial Button):** A text-link style with a custom underline using the `surface_tint` (#0053db) at 2px thickness, offset by 4px.



### Cards & Lists

- **Service Cards:** Forbid the use of divider lines. Use `spacing-10` of vertical white space to separate items. Cards use `surface_container_low` with `xl` (3rem) corner radius.

- **Input Fields:** Use `surface_container_high` backgrounds with no borders. Focus states transition the background to `surface_container_lowest` and add a 1px "Ghost Border" of the primary color.



### Key Contextual Components

- **The "Trust Bar":** A horizontal strip for testimonials or partner logos using a semi-transparent `surface_variant` background, nested within the hero section.

- **Booking Sticky Widget:** A floating "Glass" component that stays anchored to the bottom right on mobile, using high backdrop-blur and a subtle `ambient shadow`.



---



## 6. Do's and Don'ts



### Do:

* **Do** use massive corner radii (`xl` and `full`) for structural containers to match the flagship navigation style.

* **Do** use asymmetrical layouts (e.g., text left-aligned with imagery slightly offset to the right) to avoid the "bootstrap" look.

* **Do** leverage `on_surface_variant` for sub-headers to create a clear typographic hierarchy.



### Don't:

* **Don't** use 1px solid black or grey borders. They kill the premium feel.

* **Don't** use standard "drop-shadow" presets. Stick to the Ambient Shadow values (low opacity, high blur).

* **Don't** clutter the dark navigation bar. Keep links limited to 4-5 items to maintain the "Editorial" breathing room.

* **Don't** use sharp 90-degree corners anywhere in the interface.