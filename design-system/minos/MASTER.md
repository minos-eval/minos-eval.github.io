# Minos design system (master)

Source of truth for the Minos site. Page-specific overrides go in `pages/<page>.md`.
Direction came from ui-ux-pro-max (`"enterprise B2B platform trust" --design-system --variance 5 --motion 3 --density 3`):
pattern **Trust & Authority**, style **Accessible & Ethical**. Colors and type below are the brand's and override the skill's suggestions.

## Brand
- Name: MINOS. Logo: labrys mark, two colors only, never recolored.
  - Black `#1B1714` (left blade, left band, handle), red `#8F2A22` (right blade, right band).
  - On the site, the logo (`assets/minos-logo.svg`) always sits on a white surface: the floating white nav bar over the hero, and a white pill in the footer (`.on-light`). Avoid a lone white square tile on dark backgrounds; it reads like an app icon.
  - `assets/minos-logo-white-tile.svg` is kept for the favicon only.
- Do not use the old purple palette (`#2A017B`) or any purple/pink gradient.

## Typography
- Display / headings / wordmark: Montserrat 600–800.
- Body: IBM Plex Sans 400–600. Data, IDs, labels: IBM Plex Mono 400–500 (tabular figures).
- Body 17px, line-height 1.6. Headings use `text-wrap: balance`.

## Color tokens
| Token | Light | Dark |
|---|---|---|
| `--primary` | `#C8102E` | `#FF5F6D` |
| `--on-primary` | `#FFFFFF` | `#18181B` |
| `--secondary` (soft surface) | `#FDECEE` | `#2B2B2F` |
| `--bg` | `#FAFAFA` | `#18181B` |
| `--card` | `#FFFFFF` | `#212124` |
| `--sidebar` | `#F4F4F5` | `#131315` |
| `--border` | `#E5E5E8` | `#2B2B2F` |
| `--text` | `#27272A` | `#EEEEF0` |
| `--muted` | `#6B6B74` | `#A6A6AE` |

Hero gradient: `#24000A → #3D000C → #5E0014` (always rendered with dark tokens via `.on-dark`).

Status (always paired with an icon and a text label): success green, error red, warning amber, info blue, neutral zinc.
Light values are tuned to reach 4.5:1 on their tinted backgrounds.

## Rules
- Inline SVG icons (Lucide paths), never emoji.
- Illustrative UI (reports, queues) is labeled "Illustrative"; numbers from the spec are labeled as design targets.
- Comparison claims use the spec's wording ("Not documented", "Partial", "Planned"), never "No"/"Yes".
- Nav is fixed at the top on every width and compacts after scrolling; `scroll-padding-top: 96px` keeps anchors and focus clear of it.
- Focus ring 3px `--primary`; targets at least 44px; `prefers-reduced-motion` disables reveal motion.
- Responsive checks at 375 / 768 / 1024 / 1440. No horizontal scroll; wide tables scroll inside their own wrapper.
- The pilot customer stays anonymous ("a major airline") unless the team approves naming it.
