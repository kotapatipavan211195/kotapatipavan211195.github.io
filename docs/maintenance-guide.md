# Maintenance Guide

This document captures the day-to-day tasks for updating the portfolio without breaking the polished look-and-feel.

## 1. Content Updates

### Hero & About Sections
- **Headline:** Update the `<h1>` inside `.hero-main` with your current title or focus area.
- **Summary paragraph:** Revise the `<p class="subtitle">` directly under the hero title.
- **Badge chips:** Each capability is a `<span class="chip">`. Add or remove chips to match your current toolkit.
- **About list:** Located under `<div class="card hero-about">`. Keep each list item focused on AI/Data goals for consistent messaging.

### Highlights & Achievements
- Highlights live in the `.hero-high` card, achievements under the `Achievements` card in the education section.
- Each bullet uses plain `<li>` elements. Keep them short and action/resul t oriented.

### Experience & Projects
- Experience entries are `<article class="role">` nodes inside `#experience`. Tags (e.g., `data-tags="llm ingestion"`) power the filters.
  - When adding a new role, copy an existing block and adjust: `h3`, timeline, achievements list, and tech stack meta line.
- Projects follow the same pattern in `#projects`. Update the stats `<span class="pill">` values and descriptions.

## 2. Visual Tweaks

### Navigation Tabs
- Color accents are controlled via CSS variables (`--tab-about`, `--tab-skills`, etc.) near the top of `index.html`.
- To tweak a tab:
  ```css
  --tab-about: color-mix(in oklab, #hexcolor, transparent);
  ```
- Hover/active styles are defined under the `.links a` rules.

### Theme Palette
- Base colors live in the `:root` block for dark mode and the `@media (prefers-color-scheme: light)` override.
- Update both sections when adjusting palette to keep parity between themes.
- The theme toggle script sets inline CSS variables when switching modes. If you add new variables, update the `setTheme` function to maintain them.

## 3. JavaScript Behavior

Scripts are inline at the bottom of `index.html`.

- **Theme toggle:** Looks up the `#themeToggle` button, toggles CSS variables, and persists the choice via `localStorage`.
- **Scroll spy:** Uses `IntersectionObserver` to set the `.active` class on nav items based on section visibility.
- **Smooth scrolling:** Custom logic ensures anchor navigation offsets the sticky header height.
- **Filters:** Buttons in the experience section filter roles and projects by `data-tags`.

When modifying the DOM structure, ensure IDs referenced in the script continue to exist.

## 4. Deployment

This repository is configured for GitHub Pages. Follow the steps below when publishing updates:

1. Commit your changes locally.
2. Push to the `main` branch (GitHub Pages auto-deploys from `main` for user sites).
3. Wait a few minutes and confirm the site at <https://kotapatipavan211195.github.io/>.

If you relocate assets or rename the homepage file, update any references accordingly.

## 5. Accessibility Checklist
- Keep heading hierarchy logical (`h1` for hero, `h2` for section titles).
- Ensure new buttons/links have accessible text and `aria-label`s if the label isn't descriptive.
- Maintain contrast ratios when tweaking colors.
- Test keyboard navigation: Tab through the nav, CTAs, and filters after modifications.

## 6. Troubleshooting
- **Navigation highlighting stops working:** Confirm the section IDs match the `href` values in the nav.
- **Theme toggle fails:** Ensure `setTheme` continues to assign all required CSS variables.
- **Filters hide everything:** Verify each card's `data-tags` includes `all` or the specific filter keywords.

## 7. Future Ideas
- Add automated tests (e.g., Playwright or Cypress) to snapshot the layout.
- Extract CSS into a standalone file for easier caching.
- Introduce a lightweight build step (Vite, Astro, etc.) if the site grows beyond a single page.

Keep this guide updated as you evolve the site to reflect new workflows or tooling.
