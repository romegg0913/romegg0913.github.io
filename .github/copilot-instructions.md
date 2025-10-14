# Repo-specific instructions for AI agents

- Project type: simple static website (GitHub Pages) under `izuho_omi_Birthday_2025/`.
- Primary files: `top.html`, `illustration.html`, `contents.html`, `link.html`, `css/style.css`, `images/*`.

What you should do first
- Treat this as a static HTML/CSS site. No build system, no server-side code. Changes are simple edits to HTML/CSS or image assets.
- Keep markup consistent: navigation list (`ul.main-nav`) appears in each page; update all pages when changing navigation, logo, or footer.

Common tasks examples
- Add a new page: create `izuho_omi_Birthday_2025/<pagename>.html`, copy the header/nav/footer pattern from `top.html`, update `ul.main-nav` to include the new link.
- Replace logo: update `images/logo.png` or `images/logo2.svg` and ensure `img.logo` references in `top.html` and others point to the new file.
- Add gallery images: place files in `images/` and add markup inside `main.wrapper.grid` as `<div class="item"><img src="images/your.png" alt=""><p>caption</p></div>`.

Project-specific conventions
- Files are in `izuho_omi_Birthday_2025/`. Paths in HTML are relative (e.g., `css/style.css`, `images/...`) — keep relative links when editing pages.
- Navigation uses four items (Top, Illustration, Contents, Link). Maintain the same order and exact filenames when possible.
- CSS is centralized in `css/style.css`. Minimal inline styles occasionally used (e.g., centering image in `top.html`) — prefer adding/modifying classes in `style.css` for consistent styling.

Developer workflows
- There is no build step. To preview locally, open `izuho_omi_Birthday_2025/top.html` in a browser or use a static server like `python -m http.server` from the repository root.
- Commits should include updated HTML and any added images. Keep commit messages short and descriptive (e.g., "Add gallery images" or "Update navigation order").

Safety and assets
- Images appear to be included directly in the repo. Do not remove or rename existing images without updating all references (search for the filename in HTML files).

Files to reference when making edits
- Header/nav/footer template: `top.html` and `illustration.html` (consistent structure)
- Styles: `izuho_omi_Birthday_2025/css/style.css`
- Image assets: `izuho_omi_Birthday_2025/images/`

When to ask for human guidance
- If adding JS behavior, ask the repo owner—no JS currently exists and adding it may require design choices.
- When removing or drastically renaming files (logos, footer images) — confirm replacements to avoid broken pages.

If you modify multiple pages, update all occurrences of shared snippets (nav, header, footer) to keep site consistent.

---
If any of these assumptions are incorrect (for example, you have a CI/CD step or external hosting constraints), ask before making large structural changes.