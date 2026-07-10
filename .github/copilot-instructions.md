# Odd Weeks — Copilot Project Instructions

> **This is a personal project by Rahul.**  
> It is entirely unrelated to Volvo Cars work.  
> All product decisions, design rules, and briefs in this file apply only here.

---

## What is Odd Weeks?

A mobile web app for a couple (Rahul in Stockholm, Jo in Göteborg) who travel together during odd Swedish weeks. The app eliminates travel decision fatigue by curating exactly **three Weekend Briefs** — not search results, but thoughtful recommendations.

The core problem: **deciding** where to go, not booking.

---

## Product Philosophy

- Feel like a **thoughtful travel companion**, not a search engine
- Optimise for one outcome: *"Can we confidently decide in under five minutes?"*
- Never overwhelm. Never maximise choice. **Optimise for confidence.**
- Every screen should help users imagine themselves spending that weekend together

---

## Users

| Person | Location | Shape identity |
|--------|----------|----------------|
| Rahul  | Stockholm | Circle (blue `#4a6fcf`) |
| Jo     | Göteborg  | Heart (pink `#c0567a`) |

Free during **odd Swedish weeks** (ISO week numbers). Typical trip: Wednesday–Sunday.

---

## Design System — Quiet Luxury

The visual language is editorial, warm, and premium. Reference: `moodboard-quiet-luxury.png`.

### Light Mode (default)
| Token | Value | Usage |
|-------|-------|-------|
| `--bg` | `#ede9e2` | Page background (warm greige) |
| `--surface` | `#ffffff` | Cards, sheets |
| `--text-1` | `#1a1916` | Primary text (near-black) |
| `--text-2` | `#3d3b37` | Secondary text |
| `--text-3` | `#7a776f` | Eyebrow labels, metadata |
| `--accent` | `#1a1916` | CTAs, selected states (NOT amber) |
| `--border` | `rgba(0,0,0,0.08)` | Subtle borders |

### Dark Mode
| Token | Value |
|-------|-------|
| `--bg` | `#0e0d0b` |
| `--accent` | `#c9956a` (amber only in dark mode) |

### Typography
- **Headings**: Playfair Display (serif)
- **Body/UI**: Inter (sans-serif)
- Eyebrow labels: uppercase, letter-spaced, `--text-3`
- Section headings: Playfair, normal weight, `--text-1`

### Dividers ("fabric cuts")
Subtle inset shadow lines that feel like an elegant cut in the fabric of the page.
```css
border-bottom: 1px solid rgba(0,0,0,0.10);
box-shadow: 0 1px 0 rgba(255,255,255,0.7);
```

---

## Current Build

- Single-file HTML prototype: `index.html` (no build step)
- Hosted: https://rahulsen79.github.io/odd-weeks/
- All CSS, JS, and HTML in one file
- No frameworks — vanilla JS, Google Fonts CDN
- Theme toggled via `data-theme` on `<html>`, persisted in `localStorage`

---

## Rules for Copilot

1. **Personal project only** — never apply Volvo brand, systems, or constraints here
2. Always reference the Quiet Luxury moodboard for visual decisions
3. No amber (`#c9956a`) in light mode — near-black accent only
4. Preserve the single-file architecture unless explicitly asked to change it
5. Keep copy warm and editorial — avoid generic UI microcopy
6. Rahul = circle, Jo = heart — never swap these
7. When in doubt: less is more. Reduce choice, increase confidence.
