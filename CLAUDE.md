# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Git Rules

- Never add Co-Authored-By to commit messages.
- Always write commit messages in Russian.
- Always create a feature branch from main before starting a new feature (e.g. `feature/my-feature`).
- Always create a fix branch from main before starting a bug fix (e.g. `fix/broken-margins-in-button`).
- Never add "🤖 Generated with Claude Code" or similar signatures to PR descriptions.

## Project Overview

Landing page for Voice Decoder — a native macOS menu bar app for real-time voice-to-text transcription (Russian + English). Hosted on GitHub Pages.

**App repository:** `../VoiceDecoder(App)` (Swift + SwiftUI + whisper.cpp)

## Tech Stack

- **HTML** — single `index.html` with all content
- **CSS** — inline `<style>` block, no external stylesheets
- **JavaScript** — inline `<script>` block, vanilla JS only (no frameworks/libraries)
- **Hosting** — GitHub Pages, deployed from `main` branch (root)
- **Domain** — `voicedecoder.redorcdron.space` (CNAME in repo root)

## Structure

```
/
├── index.html      # Landing page (HTML + CSS + JS — all inline)
├── CNAME           # Custom domain for GitHub Pages
└── README.md       # Deploy instructions
```

## Localization

- Primary language: English
- Secondary language: Russian (via JS switcher)
- All user-facing text uses `data-i18n="key"` attributes
- Translations stored in JS object: `const i18n = { en: {...}, ru: {...} }`
- User's language choice persisted in `localStorage`

## Design

- Dark theme with indigo/purple accents
- Color palette defined in CSS `:root` variables
- Minimalist, conversion-focused layout
- Mobile-first responsive design
- Scroll animations via IntersectionObserver

## Deploy

Push to `main` → GitHub Pages auto-deploys from root.

```bash
git push origin main
```

DNS configured via Cloudflare CNAME → `xecca.github.io`.
