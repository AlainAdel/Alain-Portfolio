<!-- Auto-generated guidance for AI coding agents working on this repository -->
# Repo quick guide for automated coding agents

Purpose: help an AI agent be immediately productive editing, extending, or fixing this static portfolio site.

- Big picture
  - This is a static HTML/CSS portfolio. No build system, package.json, or server-side code.
  - Top-level entry points: `index.html` and `projects.html`.
  - Each project lives in its own folder (naming pattern like `N.M <Name> Project/`) and typically contains:
    - `index.html` (the student's attempt)
    - `solution.html` (reference solution)
    - `style.css` and an `assets/images/` subfolder when needed
  - One special folder: `4.3 HTML Porfolio Project/public/` contains exported pages (`about.html`, `contact.html`, etc.).

- Key files and directories to reference when editing
  - `index.html` — site landing page
  - `projects.html` — project listing
  - `my-favicon/` — web manifest and favicon assets (`site.webmanifest`, `favicon.ico`, svg/png icons)
  - Example project folders: `4.3 HTML Porfolio Project/`, `5.4 Color Vocab Project/`, `11.2 Bootstrap Components/`

- Project-specific patterns and conventions (do not break these)
  - Keep filenames and folder names as-is (they contain spaces and course numbering). Rename only if you update all relative links.
  - Each project uses relative paths to assets; serve files over HTTP (not file://) when validating links, because relative paths behave differently under file://.
  - Solutions are kept in `solution.html` (single-page per exercise). When improving a student file, keep the `solution.html` untouched unless explicitly asked.

- Developer workflows (how humans run/test locally)
  - There is no build step. To preview locally, either:
    - Use VS Code Live Server, or
    - From a terminal in repo root: `python3 -m http.server 8000` and open http://localhost:8000
  - Linting/tests: none present. Keep changes minimal and validate in a browser.

- Integration points & external dependencies
  - No external APIs or backends. External assets include favicons and images in `my-favicon/` and each project's `assets/`.
  - If adding third-party libraries (Bootstrap, etc.), put files locally or add a clear comment and update the top-level README (no package manager assumed).

- Editing guidance for AI agents (concrete, repo-specific)
  - When adding a new project folder, follow the existing pattern: `N.M Name Project/` with `index.html`, `solution.html`, optional `style.css`, and `assets/images/`.
  - For content/markup changes, prefer minimal diffs: edit the appropriate project's `index.html` and `style.css`. Check `solution.html` for reference patterns.
  - Preserve image filenames and paths (e.g., `5.4 Color Vocab Project/assets/images/red.png`). If you move images, update every HTML that references them.
  - Avoid mass reformatting. Small, targeted edits are preferred (this repo is a teaching portfolio — history should show small content changes).

- Examples from this repo (use these as templates)
  - Add a new image to `6.4 Motivation Meme Project/assets/images/` and reference it in that project's `index.html` using a relative path.
  - Use `4.3 HTML Porfolio Project/public/about.html` as an example of a page exported for the public site.

If anything here is unclear or you'd like more detail (e.g., preferred commit message format or a checklist for adding a new project), tell me which part to expand.

<!-- End -->