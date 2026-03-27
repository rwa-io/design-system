# RWA Design System — AI Coding Guidelines

Live styleguide: https://rwa-io.github.io/design-system/

You MUST follow these guidelines when building UI for any RWA-related project. Before creating any new component, check the styleguide link above for existing patterns. Reuse first, create second.

---

## Fonts

- **Primary:** `'Roboto', sans-serif` — weights: 300, 400, 500, 700, 900
- **Numeric Display:** `'Space Grotesk', sans-serif` — weights: 500, 600, 700
- **Monospace:** `'Roboto Mono', monospace` — weights: 400, 700
- Load from Google Fonts:
  ```
  Roboto:wght@300;400;500;700;900
  Roboto+Mono:wght@400;700
  Space+Grotesk:wght@500;600;700
  ```

## Color Palette

### Brand
| Token | Hex | Usage |
|-------|-----|-------|
| Blue | `#224BEE` | Hero gradients, eyebrow labels, links |
| Green | `#5EE4C0` | Hero gradient end, growth signals |
| Teal | `#00A38D` | Secondary CTAs, verified states |
| Gold | `#D4881A` | Premium highlights, APY accents |
| Blue Mid | `#1A6FDB` | Links, focus states, eyebrow labels |

### Navy
| Token | Hex | Usage |
|-------|-----|-------|
| Navy 900 | `#0A1628` | Sidebar, primary dark bg |
| Navy 800 | `#152238` | Dark surface secondary |
| Navy 700 | `#1D3461` | Dark surface tertiary |
| Blue 500 | `#1A6FDB` | Links, focus, eyebrow labels |
| Blue 400 | `#4A9FF5` | Accents, highlights |

### Blue Tints
| Token | Hex | Usage |
|-------|-----|-------|
| Blue 100 | `#D4E8FD` | Info badge backgrounds |
| Blue 50 | `#E6F0FB` | Tinted surfaces |

### Neutral
| Token | Hex | Usage |
|-------|-----|-------|
| Gray 900 | `#1A1C1E` | Body text |
| Gray 700 | `#3D3F42` | Secondary text |
| Gray 500 | `#6B6E73` | Muted labels |
| Gray 400 | `#A8ABB0` | Placeholder text |
| Gray 200 | `#D6D8DB` | Borders, dividers |
| Gray 50 | `#F2F3F4` | Page bg |
| White | `#FFFFFF` | Card surfaces |

### Semantic
| Token | Hex | Usage |
|-------|-----|-------|
| Success | `#1A6644` | Active, confirmed |
| Danger | `#D44C1D` | Failed, destructive actions |
| Warning | `#B37A0A` | Pending, caution |

### Dark Mode (CSS custom properties)
| Token | Light | Dark |
|-------|-------|------|
| `--dm-bg` | `#F7F9FC` | `#0D1117` |
| `--dm-surface` | `#ffffff` | `#161B22` |
| `--dm-surf2` | `#F0F4F8` | `#1C2230` |
| `--dm-ink` | `#0C111D` | `#E6EDF3` |
| `--dm-muted` | `#6B7280` | `#8B949E` |
| `--dm-border` | `rgba(10,22,40,.1)` | `rgba(255,255,255,.1)` |
| `--dm-divider` | `#E5E7EB` | `#21262D` |
| `--dm-header` | `#ffffff` | `#161B22` |
| `--dm-stroke` | `#D6D8DB` | `rgba(255,255,255,.18)` |

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
| r-full | 100px | Pills, avatars |

## Shadows

| Level | Value | Usage |
|-------|-------|-------|
| shadow-1 | `0 1px 3px rgba(10,22,40,.06)` | Resting card elevation |
| shadow-2 | `0 4px 16px rgba(10,22,40,.10)` | Hover lift, popovers |
| shadow-3 | `0 12px 40px rgba(10,22,40,.14)` | Modals, drawers |
| shadow-accent | `0 8px 28px {accent}1A` | Hover glow on colored components (accent color at 10% opacity) |

## Typography Scale

### Casing Rules
- **Headings (H1–H4):** Title Case
- **Eyebrow labels:** Uppercase with letter-spacing `.14em`
- **Body & captions:** Sentence case
- **Buttons & CTAs:** Title Case
- **Data labels:** Preserve acronyms (APY, TVL, NAV, KYC, ETH stay uppercase)
- **No `textTransform: uppercase`** in CSS — use letter-spacing + font-weight + Title Case in source strings instead

### Website
| Element | Weight | Size | Line-height | Letter-spacing |
|---------|--------|------|-------------|----------------|
| Eyebrow | Bold | 11px | — | .14em, uppercase |
| H1 Hero | Bold | 64px | 1.0 | -.04em |
| H2 Section | Bold | 46px | 1.05 | -.03em |
| H3 Feature | Regular | 22px | 1.3 | -.01em |
| Body | Regular | 16px | 1.6 | — |

### App UI
| Element | Weight | Size | Line-height | Letter-spacing |
|---------|--------|------|-------------|----------------|
| Page Title | Bold | 24px | 1.2 | -.02em |
| Section | Bold | 18px | 1.3 | -.01em |
| Card Title | Medium | 15px | 1.4 | — |
| Label | Bold | 11px | — | .08em |
| Body | Regular | 13px | 1.5 | — |
| Numeric Hero | Space Grotesk Bold | 32px | — | -.02em |
| Numeric Inline | Roboto Medium | 13px | — | — |

## Motion

### Easing
| Token | Value | Usage |
|-------|-------|-------|
| ease-out | `cubic-bezier(0,0,.2,1)` | Entrances, slide-ins |
| ease-spring | `cubic-bezier(.34,1.56,.64,1)` | Button hover, popups |

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
| bp-md | 648px | Mobile L — 2-col unlocks |
| bp-lg | 1024px | Tablet — sidebar nav |
| bp-xl | 1280px | Desktop — 3-col grid |
| bp-2xl | 1536px | Wide — max 1200px centered |

## Grid System

| Breakpoint | Columns | Gutter | Margin |
|------------|---------|--------|--------|
| Mobile (375px+) | 4 | 16px | 16px |
| Tablet (768px+) | 8 | 24px | 24px |
| Desktop (1024px+) | 12 | 24px | 32px |
| Wide (1280px+) | 12 | 32px | 48px |
| Max (1536px+) | 12 | 32px | auto |

---

## Component Rules

### Buttons
- **Pill-shaped** always: `border-radius: 100px`
- Sizes: lg (`14px 32px` / 16px), md (`11px 24px` / 14px), sm (`7px 16px` / 12px), xs (`4px 10px` / 11px)
- Font: Roboto Bold, letter-spacing .01em
- Transition: `all 150ms` with spring easing on hover
- Disabled: `opacity: .75`, `cursor: not-allowed`, fontWeight 600

| Variant | Background | Text | When to use |
|---------|-----------|------|-------------|
| Primary | `linear-gradient(135deg, #224BEE, #1A6FDB)` + `box-shadow: 0 4px 14px rgba(34,75,238,.35)` | white | Main CTA — 1 per view max |
| Secondary | `#00A38D` | white | Key onboarding (wallet connect, tokenize) |
| Outline | transparent, `2px solid #224BEE` | `#224BEE` | Secondary action alongside filled button |
| Ghost | transparent, `1.5px solid var(--dm-stroke)` | `var(--dm-muted)`, fontWeight 500 | Tertiary — cancel, dismiss |
| Danger | `#D44C1D` | white | Destructive action, always requires confirmation |

### Badges
- Rounded: `border-radius: 100px`
- Font: 13px, fontWeight 600
- Padding: `6px 14px`
- Include a 7px colored dot before label text

#### Status
| Badge | Text Color | Background | Dot |
|-------|-----------|------------|-----|
| Active | `#166534` | `#DCFCE7` | `#16A34A` |
| Processing | `#1D4ED8` | `#DBEAFE` | `#3B82F6` |
| Pending | `#92400E` | `#FEF3C7` | `#F59E0B` |
| Failed | `#991B1B` | `#FEE2E2` | `#EF4444` |
| Inactive | `#374151` | `#F3F4F6` | — (border `#E5E7EB`) |

#### Asset Type
| Badge | Text Color | Background |
|-------|-----------|------------|
| Real Estate | `#0F766E` | `#CCFBF1` |
| Commodities | `#92400E` | `#FEF3C7` |
| Fixed Income | `#1D4ED8` | `#DBEAFE` |
| Agriculture | `#166534` | `#DCFCE7` |
| Infrastructure | `#374151` | `#F3F4F6` (border `#E5E7EB`) |

#### Compliance
| Badge | Text Color | Background |
|-------|-----------|------------|
| KYC Verified | `#0F766E` | `#CCFBF1` |
| Reg D | `#1D4ED8` | `#DBEAFE` |
| ERC-3643 | `#6D28D9` | `#EDE9FE` |
| Under Review | `#92400E` | `#FEF3C7` |
| Reg S | `#374151` | `#F3F4F6` (border `#E5E7EB`) |

### Form Inputs
- Background: `var(--dm-surface)`
- Border: `1.5px solid var(--dm-border)` (default), `#224BEE` (focused)
- Border radius: 8px
- Padding: `11px 14px`
- Focus ring: `box-shadow: 0 0 0 3px rgba(34,75,238,.10)`
- Error state: `#D44C1D` border
- Valid state: `#1A6644` border
- Disabled: `opacity: .5`, `cursor: not-allowed`
- Layout: 2-column grid (`1fr 1fr`) for side-by-side fields

### Cards
- Background: `var(--dm-surface)` (light: white / dark: `#161B22`)
- Border: `1px solid var(--dm-border)`
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
- Hero numbers: `Space Grotesk` Bold 32px, letter-spacing -.02em
- Inline numbers: `Roboto` Medium 13px
- Use `font-family: var(--font-numeric)` CSS variable for hero/display numbers
- Financial data (price, APY, TVL) is always visually prominent

### Toasts / Alerts
- Border-radius: 8px
- Left accent border: 3px solid (color matches severity)
- Background tinted to match severity
- Include icon + title + description

### Modals
- Overlay: `rgba(10,22,40,.45)` with backdrop blur
- Card: `var(--dm-surface)`, border-radius 16px, shadow-3
- Max-width: 480px, centered
- Padding: 32px

### Navigation Sidebar
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
5. **Space Grotesk for hero numbers** — Display financial figures use Space Grotesk Bold. Inline numbers use Roboto Medium.
6. **Consistent motion** — Use the defined easing curves and durations. No arbitrary animations.
7. **Reuse tokens** — Never hardcode colors, spacing, or radii. Use CSS custom properties from this guide.
