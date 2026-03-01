# alanbrantley-site-v5 Session Handoff — 2026-03-01

## Session Summary
Updated all site copy, added A/B style picker module, locked in left-aligned layout, scaled hero text, boosted dark mode contrast, and removed footer email.

## Git Status

| Field | Value |
|-------|-------|
| Branch | `main` |
| Latest | `13480fe` style: lock in left-aligned layout, hide A/B picker |
| Status | Clean |

## What's Shipped
- Updated all five copy sections (hero, about, three project panels)
- Added A/B style picker module (CSS, JS, HTML) — currently hidden, preserved for future tests
- Left-aligned layout (Style B) locked in as default
- Hero text scaled up (name: 2.4rem, statement: 1.5625rem)
- Dark mode contrast boosted (--fg3: #777, --fg4: #555)
- Removed footer email link
- Mobile responsive fix: style picker tucks in on small screens, panel max-height increased to 260px

## Known Issues
- None

## Blockers
- None

## Learnings
- **Project moved:** Repo relocated from `~/alanbrantley-site-v5` to `~/Developer/alanbrantley-site-v5`
- **A/B picker pattern:** `data-style` attribute on `<html>` with `localStorage` persistence — same pattern as theme toggle. Hidden with `display:none`, ready to unhide for next test.
- **Dark mode contrast:** Original --fg4: #333 was nearly invisible on --bg: #0d0d0d. Needed significant bump.

## Next Actions
1. [ ] Test mobile layouts across devices
2. [ ] Plan next A/B test using the preserved picker module
3. [ ] Consider whether container max-width (420px) should scale with larger hero text

## Key Files
- `index.html` — Entire site (HTML, CSS, JS inline)
- `CLAUDE.md` — Claude Code context file
