# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Repository Is

A static website that hosts legal documents for the **FDNY Mutual Tracker** mobile app. It has no build system, no dependencies, and no tests — just two standalone HTML files served as-is (e.g., via GitHub Pages or any static host).

## Files

- `index.html` — Standalone Privacy Policy page (effective April 27, 2026)
- `legal.html` — Combined Terms of Use + Privacy Policy page (more recent; last updated June 7, 2026 for ToU, April 28, 2026 for Privacy)

`legal.html` is the canonical, more complete document. `index.html` is the older, simpler privacy-only page. If privacy policy content diverges between the two, `legal.html` takes precedence.

## About the App

FDNY Mutual Tracker is an iOS/Android scheduling aid for adult FDNY firefighters. Key facts relevant to editing these documents:

- **No backend**: all data (group number, mutual history, RSOT dates, overtime logs) is stored locally using `AsyncStorage`; nothing is transmitted to external servers.
- **Subscription model**: 7-day free trial → $9.99/year auto-renewing, billed via Apple App Store and Google Play, processed through **RevenueCat**.
- **Third-party disclosure required**: RevenueCat, Apple, and Google handle billing; their privacy policies must be linked when mentioning subscription/billing.
- **Not affiliated with FDNY/NYC Fire Department** — disclaimers to this effect must be maintained.
- **Contact email**: fdnyscheduler@gmail.com

## Editing Conventions

- Both files use inline `<style>` blocks; there is no external CSS.
- When updating effective/last-updated dates, update them in both files if the same policy section is changed.
- `legal.html` uses anchor IDs (`#terms`, `#privacy`) for in-page navigation; preserve these when restructuring sections.
- The color palette: primary red `#b22222`, link blue `#1a73e8` (index.html) / primary red `#b22222` (legal.html).
