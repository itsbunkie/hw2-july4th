# Stars & Stripes Canvas

A three-chapter, CSS-only Independence Day storybook. No JavaScript is used anywhere in the project.

## Files

- `index.html` — semantic HTML5 markup for all three chapters
- `stars-and-stripes.css` — the single stylesheet (palette, layout, animation, interactivity)
- `assets/images/` — PNG assets for every non-emoji graphic: `flag.png`, `star.png`, `sun.png`, `burst.png`, `rocket.png`

## Chapters

1. **Freedom's Dawn** — a sunrise hero with a rising/waving flag (`flag.png`), plus a `:checked`-driven sparkler toggle (`star.png`).
2. **Patriot's Plaza** — a Main Street parade with `translateX` marchers (emoji) and a `:checked` radio group that swaps between three float descriptions.
3. **United We Stand** — a night-sky fireworks finale with a `:checked`-driven launcher (`rocket.png` + `burst.png`) and a closing statement.

## CSS techniques used

- CSS variables for the full color palette and spacing scale
- `:target` for the three-page navigation (no JavaScript router)
- `:checked` for the sparkler toggle, fireworks launcher, and float picker
- `:hover` / `:focus-visible` micro-interactions on every link, label, and card
- `@keyframes` animations restricted to `transform` and `opacity` (GPU-compositable)
- `nth-child`-based staggering where multiple elements share one animation
- CSS Grid for the card layouts, Flexbox for the header/nav
- `prefers-reduced-motion` support that shortens every animation to near-zero
- Mobile-first layout with a single `min-width: 700px` breakpoint
