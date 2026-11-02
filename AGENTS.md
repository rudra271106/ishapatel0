# AGENTS.md

## Architecture
A static single-page site with no framework and no build step. All markup, styles, and scripts live in `index.html`. `netlify.toml` publishes the repo root.

## Key details
- The Telegram invite URL appears twice in `index.html`: once in the `href` of `#joinBtn` and once in the `TELEGRAM_URL` constant in the script. If the link changes, update both.
- The countdown length is set by `TOTAL_SECONDS` (15). The redirect fires when it reaches 0. Clicking the button stops the timer.
- Theme colors are CSS custom properties defined in `:root`.
- The avatar image loads from Unsplash.

## Conventions
Keep the site as a single static file unless the scope grows. Don't add a bundler or framework just for small changes.
