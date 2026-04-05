# alanbrantley-site-v5 — Project state

## Where we are
v5 static landing page is shipped and live. Left-aligned layout locked in. All copy updated. A/B picker module built but hidden. Most recent work was updating project panel descriptions and hero statement copy.

## Implemented
- Static single-page landing site with hero, project tabs, about section
- Light/dark theme toggle with localStorage persistence
- Staggered fade-up entry animations
- Responsive layout (480px breakpoint)
- Left-aligned layout (Style B) as default
- A/B style picker module (hidden via `display:none`, preserved for reuse)
- Updated copy across all sections (hero, about, three project panels)
- Hero text scaled up (name: 2.4rem, statement: 1.5625rem)
- Boosted dark mode contrast (--fg3: #777, --fg4: #555)
- Footer email link removed
- CLAUDE.md for Claude Code context

## Stubbed or missing
- Mobile testing across devices not yet done
- A/B picker hidden — no active test running

## Known issues
- None

## Architecture
- Single `index.html` with inline CSS and JS — no build step, no dependencies
- Deployed as static HTML to Vercel
- `data-theme` attribute on `<html>` toggles light/dark with localStorage persistence
- `data-style` attribute on `<html>` for A/B layout switching (currently unused)
- docs/ in repo is source of truth for project documentation
- Symlinked into Obsidian vault for Claude.ai access

## Decisions locked
- Left-aligned layout (Style B) is the default — A/B picker hidden, not removed
- Dark mode contrast values: --fg3: #777, --fg4: #555 (original --fg4: #333 was nearly invisible)
- Project repo lives at ~/Developer/alanbrantley-site-v5

## Recent
- 2026-04-05: Project scaffolded with docs/ state management (migrated from old SESSION_HANDOFF.md / PROJECT_STATE.md / SESSION_LOG.md)
- 2026-03-01 (a2e3e70): Updated project panel descriptions
- 2026-03-01 (c2e6e27): Updated hero statement copy
- 2026-03-01 (f3c0078): Refreshed site copy and synced session tracking
- 2026-03-01 (13480fe): Locked in left-aligned layout, hid A/B picker

## Next
1. Test mobile layouts across devices
2. Plan next A/B test using preserved picker module
3. Consider whether container max-width (420px) should scale with larger hero text
