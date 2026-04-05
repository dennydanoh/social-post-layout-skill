# Social Post Layout Skill

Reusable Codex skill for turning long-form content into publish-ready social post cards, editorial image carousels, and poster-style pages.

## What It Includes

- A browser-based static web tool
- Fixed cover and body-page layout
- Light editorial visual style
- Editable solid-color or image background
- Automatic pagination
- Browser-side PNG export
- Local draft persistence in the browser

## Repository Structure

- `SKILL.md`: skill trigger rules and workflow guidance for Codex
- `assets/social-post-tool/index.html`: tool UI
- `assets/social-post-tool/styles.css`: visual system and layout
- `assets/social-post-tool/app.js`: pagination, persistence, rendering, and PNG export

## Best Fit

Use this skill when you want to:

- Turn a long article into social post cards
- Generate editorial poster pages from text content
- Keep everything static and browser-side
- Export ready-to-publish PNG pages without adding a backend
- Extend the tool later with login, subscriptions, analytics, or cloud drafts

## Installation

Clone this repository and install it as a Codex skill, or copy the skill directory into your local skills workspace.

## Notes

- The bundled tool is local-first and browser-side by default.
- The default export ratio is vertical `3:4`.
- If you later add login, payments, or cloud sync, keep secrets and billing logic behind server routes.
