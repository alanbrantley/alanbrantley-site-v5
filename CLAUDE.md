# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Personal landing page for alanbrantley.com. Single-file static site — no build step, no dependencies, no package manager.

## Architecture

Everything lives in `index.html`: markup, CSS (in `<style>`), and JS (in `<script>`). Deployed as static HTML to Vercel.

## Development

Open `index.html` in a browser. No server required, though `python3 -m http.server` or similar works if needed.

## Design System

- **Fonts:** DM Sans (body) and DM Mono (labels/UI) via Google Fonts
- **Theming:** `data-theme` attribute on `<html>` toggles light/dark. CSS custom properties defined per theme in `[data-theme="light"]` / `[data-theme="dark"]` blocks
- **Design tokens:** `--bg`, `--fg`, `--fg2`, `--fg3`, `--fg4`, `--rule`, `--hover`, `--grain` — treat these as read-only unless explicitly asked to update the color system
- **Transitions:** All theme transitions use `--ease` (cubic-bezier). Grain overlay on `body::after`
- **Layout:** Centered single column, max-width 420px. Responsive breakpoint at 480px

## Interactive Patterns

- **Project tabs:** Click-to-toggle panels using `data-target` attributes and `.open` class. Only one panel open at a time
- **About section:** Collapsible body toggled by `.about-toggle` button
- **Theme toggle:** Fixed top-right button, persists preference in `localStorage`
- **Entry animations:** Staggered fade-up using `.fade` + delay classes `.d1`–`.d5`
