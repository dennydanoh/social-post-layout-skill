---
name: social-post-layout-generator
description: Use this skill when the user wants to turn long-form content into publish-ready social post cards, editorial image carousels, or poster-style pages with a fixed light template, editable background, auto pagination, and browser-side PNG export. Also use it when editing or deploying the bundled web tool.
---

# Social Post Layout Generator

This skill packages a browser-based tool for turning long-form content into publish-ready social cards, editorial image carousels, and poster-style pages.

## Use when

- The user wants to turn a long article into social post cards or editorial poster pages
- The user wants a fixed cover page and body-page layout
- The user wants browser-side PNG export
- The user wants to edit, redesign, or deploy the bundled web tool

## Files

- `assets/social-post-tool/index.html`: tool UI
- `assets/social-post-tool/styles.css`: visual system and layout
- `assets/social-post-tool/app.js`: pagination, persistence, rendering, and PNG export

## Workflow

1. Keep the tool static and browser-side by default.
2. Preserve the default vertical 3:4 export ratio unless the user asks to change platform format.
3. Keep the light editorial visual direction unless the user explicitly asks for a redesign.
4. Treat the first exported page as the cover and paginate the remaining article into body pages.
5. Prefer local persistence and client-side export unless the user explicitly asks for login, sync, or server storage.

## Guardrails

- Do not introduce server-only rendering unless the user asks for backend features.
- Do not depend on third-party CDN fonts or runtime libraries unless clearly necessary.
- Do not store secrets in the frontend.
- If login, subscriptions, or cloud drafts are added, move those capabilities behind server routes and keep the current tool usable as a local-first fallback.
