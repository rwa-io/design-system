# RWA Design System — AI Coding Guidelines

Live styleguide: https://rwa-io.github.io/design-system/

You MUST follow these guidelines when building UI for any RWA-related project. Before creating any new component, check the styleguide link above for existing patterns. Reuse first, create second.

---

## Fonts

- **Primary:** `'Roboto', sans-serif` — weights: 300, 400, 500, 700, 900
- **Monospace:** `'Roboto Mono', monospace` — weights: 400, 500
- Load from Google Fonts:
  ```
  Roboto:wght@300;400;500;700;900
  Roboto+Mono:wght@400;500
  ```

## Color Palette

### Brand
| Token | Hex | Usage |
|-------|-----|-------|
| Blue | `#224BEE` | Hero gradients, eyebrow labels, links |
| Green | `#5EE4C0` | Hero gradient end, brand accent |
| Teal | `#00A38D` | Secondary CTAs, verified states |
| Gold | `#D4881A` | Premium highlights, APY |
| UI Blue | `#0052FF` | Primary CTA buttons, focus rings |
| Red/Danger | `#D73848` | Destructive actions |

### Text
| Token | Hex | Usage |
|-------|-----|-------|
| Ink | `#0C111D` | Headings |
| Body | `#1A2233` | Body text |
| Muted | `#6B7280` | Secondary text |
| Muted2 | `#4B5563` | Tertiary text |

### Neutrals
| Token | Hex |
|-------|-----|
| N900 | `#0C111D` |
| N600 | `#475467` |
| N400 | `#98A2B3` |
| N300 | `#D1D5DB` |
| N100 | `#F2F4F7` |

### Semantic
| Token | Hex |
|-------|-----|
| Success | `#0E9E5A` |
| Error | `#DC2626` |
| Warning | `#D97706` |
| Info | `#2563EB` |

### Dark Mode
- Background: `#0A1628` (Navy)
- Primary text: `#FFFFFF`
- Secondary text: `rgba(255,255,255,.6)`
- Tertiary text: `rgba(255,255,255,.3)`

## Spacing

| Token | Value | Usage |
|-------|-------|-------|
| space-1 | 4px | Inline gaps, icon padding |
| space-2 | 8px | Internal component gaps |
| space-3 | 12px | Small card padding |
| space-4 | 16px | Default padding, row gap |
| space-5 | 24px | Section gap, card padding |
| space-6 | 32px | Section spacing |
| space-8 | 48px | Page horizontal padding |
| space-10 | 72px | Major section breaks |

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| r-sm | 6px | Badges, chips |
| r-md | 8px | Inputs, buttons |
| r-lg | 12px | Cards, panels |
| r-xl | 16px | Form cards, modals |
| r-2xl | 20px | Hero strips |
| r-pill | 100px | Pill buttons, pill badges |

## Shadows

| Level | Value | Usage |
|-------|-------|-------|
| shadow-1 | `0 1px 3px rgba(10,22,40,.06)` | Resting elevation |
| shadow-2 | `0 4px 16px rgba(10,22,40,.10)` | Hover lift, popovers |
| shadow-3 | `0 12px 40px rgba(10,22,40,.14)` | Modals, drawers |

## Typography Scale

### Website
| Element | Weight | Size | Line-height | Letter-spacing |
|---------|--------|------|-------------|----------------|
| Eyebrow | Bold | 11px | — | .16em, uppercase |
| H1 Hero | Bold | 64px | 1.0 | -.04em |
| H2 Section | Bold | 46px | 1.05 | -.03em |
| H3 Feature | Regular | 22px | 1.3 | -.01em |
| Body | Regular | 16px | 1.6 | — |
| Button | Bold | 13px | — | .01em |
| Link | Bold | 13px | — | Brand Blue |

### App UI
| Element | Weight | Size | Line-height | Letter-spacing |
|---------|--------|------|-------------|----------------|
| Page Title | Bold | 24px | 1.2 | -.02em |
| Section | Bold | 18px | 1.3 | -.01em |
| Card Title | Medium | 15px | 1.4 | — |
| Label | Bold | 11px | — | .08em, uppercase |
| Body | Regular | 13px | 1.5 | — |
| Caption | Regular | 11px | 1.4 | Muted |
| Numeric Hero | Mono Light | 32px | — | -.02em, tabular-nums |
| Numeric Inline | Mono Medium | 13px | — | tabular-nums |

## Motion

### Easing
| Token | Value | Usage |
|-------|-------|-------|
| ease-out | `cubic-bezier(0,0,.2,1)` | Entrances, slide-ins |
| ease-in | `cubic-bezier(.4,0,1,1)` | Exits, fade-outs |
| ease-spring | `cubic-bezier(.34,1.56,.64,1)` | Button hover, popups |
| ease-smooth | `cubic-bezier(.4,0,.2,1)` | Layout transitions |

### Duration
| Token | Value | Usage |
|-------|-------|-------|
| dur-fast | 150ms | Micro-interactions, hover |
| dur-base | 250ms | Panels, modals, cards |
| dur-slow | 400ms | Page-level transitions |

## Breakpoints

| Token | Value | Usage |
|-------|-------|-------|
| bp-sm | 375px | Mobile S — single column |
| bp-md | 640px | Mobile L — 2-col unlocks |
| bp-lg | 1024px | Tablet — sidebar nav |
| bp-xl | 1280px | Desktop — 3-col grid |
| bp-2xl | 1536px | Wide — max 1200px centered |

---

## Component Rules

### Buttons
- **Pill-shaped** always: `border-radius: 100px`
- Sizes: lg (`12px 26px`), md (`9px 20px`), sm (`6px 13px`)
- Font: Roboto Bold 13px, letter-spacing .01em
- Transition: `all 150ms` with spring easing on hover
- Disabled: `opacity: .32`, `cursor: not-allowed`

| Variant | Background | Text | When to use |
|---------|-----------|------|-------------|
| Primary | `#0052FF` | white | Main CTAs |
| Teal | `#00A38D` | white | Wallet connect, tokenize |
| Outline | transparent, 1.5px border `#D1D5DB` | `#1A2233` | Secondary actions |
| Ghost | transparent | `#6B7280` | Tertiary, cancel, nav |
| Danger | `#D73848` | white | Delete, revoke |

### Badges
- Rounded: `border-radius: 100px`
- Font: Roboto Bold, uppercase, letter-spacing .04em
- Sizes: xs/sm (9px), md (11px)
- Include a small colored dot before label text

| Variant | Background | Text |
|---------|-----------|------|
| Success | `#DCFCE7` | `#15803D` |
| Info | `#DBEAFE` | `#1D4ED8` |
| Warning | `#FEF3C7` | `#B45309` |
| Error | `#FEE2E2` | `#B91C1C` |
| Teal | `#CCFBF1` | `#0F766E` |
| Gold | `#FEF9C3` | `#92400E` |
| Neutral | `#F3F4F6` | `#4B5563` |

### Form Inputs
- Background: `#F8F9FB` (default), `#fff` (focused)
- Border: `1px solid #D1D5DB` (default), `#0052FF` (focused)
- Border radius: 8px
- Padding: `10px 13px`
- Focus ring: `box-shadow: 0 0 0 3px rgba(0,82,255,.10)`
- Error state: `#DC2626` border
- Valid state: `#16A34A` border
- Disabled: `opacity: .5`, `cursor: not-allowed`
- Layout: 2-column grid (`1fr 1fr`) for side-by-side fields

### Cards
- Background: white (light) / `#0F1D32` (dark)
- Border: `1px solid #F2F3F4`
- Border radius: 12px
- Padding: 24px
- Hover: shadow-2 lift
- Asset cards use a left accent stripe (3px) color-coded by asset class:
  - Real Estate: `#1A6FDB`
  - Agriculture: `#00A38D`
  - Infrastructure: `#D4881A`
  - Fixed Income: `#224BEE`
  - Commodities: `#0F766E`

### Data & Numbers
- Always use `Roboto Mono` for financial figures
- Use `font-variant-numeric: tabular-nums` for alignment
- Hero numbers: Light 32px
- Inline numbers: Medium 13px

### Toasts / Alerts
- Border-radius: 8px
- Left accent border: 3px solid (color matches severity)
- Background tinted to match severity
- Include icon + title + description

### Modals
- Overlay: `rgba(10,22,40,.45)` with backdrop blur
- Card: white, border-radius 16px, shadow-3
- Max-width: 480px, centered
- Padding: 32px

### Navigation Sidebar (if applicable)
- Width: 232px, sticky left
- Background: `#0A1628` (dark navy)
- Active item: left 2px border `#1A6FDB`, bg `rgba(26,111,219,.18)`
- Hover: `rgba(255,255,255,.04)` background

---

## Design Principles

1. **Institutional grade** — Professional, finance-focused aesthetic. No playful/casual UI.
2. **Price-first hierarchy** — Financial data (price, APY, TVL) is always prominent.
3. **Typography carries identity** — No heavy icon reliance in cards. Color and type do the work.
4. **Class-coded accents** — Asset classes have unique accent colors.
5. **Monospace for money** — All financial figures use Roboto Mono with tabular numerals.
6. **Consistent motion** — Use the defined easing curves and durations. No arbitrary animations.
7. **Reuse tokens** — Never hardcode colors, spacing, or radii. Use the values from this guide.
