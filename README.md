# RWA Design System

Live styleguide: **https://rwa-io.github.io/design-system/**

Design tokens, components, and visual guidelines for building consistent RWA (Real World Assets) interfaces with AI coding tools.

## Usage with AI Tools

### Lovable / Replit / Bolt

Paste this in your first prompt:

> Follow the design system at https://rwa-io.github.io/design-system/ — use Roboto font, pill-shaped buttons (#0052FF primary), 12px card radius, Roboto Mono for all numbers. Match the colors, spacing, and component patterns shown there.

For best results, screenshot specific sections from the styleguide and attach them to your prompt. These tools respond well to visual references.

### Claude Code / Codex

Copy `CLAUDE.md` from this repo into the root of your project. Claude Code and Codex automatically read this file and will follow the design tokens and component rules defined in it.

```bash
# From your project root
curl -O https://raw.githubusercontent.com/rwa-io/design-system/main/CLAUDE.md
```

That's it — every component Claude or Codex generates will follow the system.
