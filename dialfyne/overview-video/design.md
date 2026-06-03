# Dialfyne — Design System (overview video)

Premium SaaS launch explainer. Dark, cinematic, confident. Think Linear / Vercel / Stripe
launch films, recolored to Dialfyne's sky-blue. Brand voice: human, direct, no em dashes.

## Palette

| Token         | Hex       | Use                                          |
| ------------- | --------- | -------------------------------------------- |
| ink           | `#070B14` | Primary background (near-black, blue-tinted) |
| ink-panel     | `#0E1626` | Elevated panels / cards                      |
| hairline      | `#1C2840` | Borders, dividers, grid lines                |
| fg            | `#F4F8FF` | Primary text (off-white)                     |
| muted         | `#A9BBD6` | Secondary text, labels                       |
| accent-sky    | `#7FC3F7` | Brand light blue — focal numbers, headlines  |
| accent-bright | `#3FA9FF` | Brighter focal hits, glows                   |
| accent-deep   | `#1B6FE8` | Brand gradient end, deep accent              |

Background is always `ink`. One accent hue (brand blue) across all scenes. Tint neutrals cool.

## Typography

- **Display:** Oswald (condensed grotesque). Headlines & big numbers at 700. Light body/tagline at 300.
- **Mono:** JetBrains Mono. Labels, units, metadata, technical readouts at 500-700.
- Weight contrast is extreme (300 vs 700). Condensed display gives the big stats height.
- Tension: condensed display (poster-confident) vs precise mono (technical) = launch energy + engineered trust.
- Both are renderer-bundled fonts (auto-resolved). `font-variant-numeric: tabular-nums` on all stacked numbers.

## Motion

- Confident, kinetic, restrained. Vary eases (3+ per scene) and durations (fastest ~0.25s,
  slowest ~0.8s). Big numbers SLAM/COUNT. Decoratives breathe/pulse (finite repeats only).
- Primary transition character: directional blur crossfades. ONE hero moment: zoom-through
  into the brand reveal. Outro winds down with a slow focus pull.

## Don'ts

- No em dashes anywhere on screen (brand rule). Use periods and short lines.
- No gradient text, no left-edge accent stripes, no cyan neon, no pure #000/#fff.
- No corporate jargon. Lead with the pain. Human, peer-level copy.
- No `repeat: -1`. No exit animations except the final scene. Transitions handle exits.
