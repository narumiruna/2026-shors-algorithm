# Repository Guidelines

## Project Structure & Module Organization
This repository is a single-page static site focused on Shor's algorithm and crypto risk education.

- `index.html`: page structure and all content sections.
- `style.css`: visual system, layout, and responsive behavior.
- `data/`: reference source files (PDF papers/whitepapers) used by the page.
- `README.md`: minimal project identifier.

Keep responsibilities explicit: content and semantics in `index.html`, presentation in `style.css`, source artifacts in `data/`.

## Build, Test, and Development Commands
No build pipeline is required. Use a local static server for development:

- `python -m http.server 8000`: serve the repo at `http://localhost:8000`.
- `uv run ruff check .`: lint Python utilities if any are added.
- `uv run ruff format .`: format Python files if any are added.
- `uv run ty check .`: run type checks for Python files if introduced.

If `.pre-commit-config.yaml` exists and code/config is changed, run `prek run -a` (fallback: `pre-commit run -a`).

## Coding Style & Naming Conventions
- Use 2-space indentation in HTML/CSS, matching current files.
- Prefer semantic, descriptive IDs/classes (e.g., `#sidebar`, `.stat-card`, `.info-box`).
- Keep CSS variables in `:root` for theme consistency.
- Avoid inline styles and avoid mixing content logic into CSS names.
- Keep files under 1000 lines; split by responsibility if a file exceeds ~500 lines.

## Testing Guidelines
There is no automated test suite yet. For each change:

- Validate desktop and mobile layouts manually.
- Verify sidebar navigation anchors and section jumps.
- Confirm external assets (MathJax CDN and `data/*.pdf` links) still load.

For non-trivial future logic changes, follow TDD (red -> green -> refactor) and add focused tests before implementation.

## Commit & Pull Request Guidelines
- Use scoped, imperative commit messages (e.g., `docs: clarify quantum timeline section`, `style: improve mobile sidebar spacing`).
- Stage files explicitly (`git add index.html style.css`), not broad staging.
- PRs should include: purpose, changed files, before/after screenshots for UI-impacting edits, and manual verification steps.
- Keep each PR focused on one objective; avoid mixing content updates with unrelated refactors.
