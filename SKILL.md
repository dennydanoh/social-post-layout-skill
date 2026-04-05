---
name: xiaohongshu-post-generator
description: Use this skill when the user wants to turn a full Chinese article into a Xiaohongshu-style image carousel with a fixed light template, editable background, cover page, auto pagination, and browser-side PNG export. Also use it when editing or deploying the bundled web tool.
---

# Xiaohongshu Post Generator

This skill packages a browser-based Xiaohongshu carousel generator as reusable assets.

## Use when

- The user wants to turn a long Chinese article into Xiaohongshu image cards
- The user wants a fixed cover page and body-page layout
- The user wants browser-side PNG export
- The user wants to edit, redesign, or deploy the bundled web tool

## Files

- `assets/xhs-post-tool/index.html`: tool UI
- `assets/xhs-post-tool/styles.css`: visual system and layout
- `assets/xhs-post-tool/app.js`: pagination, persistence, rendering, and PNG export

## Workflow

1. Keep the tool static and browser-side by default.
2. Preserve the vertical 3:4 export ratio unless the user asks to change platform format.
3. Keep the light editorial visual direction unless the user explicitly asks for a redesign.
4. Treat the first exported page as the cover and paginate the remaining article into body pages.
5. Prefer local persistence and client-side export unless the user explicitly asks for login, sync, or server storage.

## Guardrails

- Do not introduce server-only rendering unless the user asks for backend features.
- Do not depend on third-party CDN fonts or runtime libraries unless clearly necessary.
- Do not store secrets in the frontend.
- If login, subscriptions, or cloud drafts are added, move those capabilities behind server routes and keep the current tool usable as a local-first fallback.
