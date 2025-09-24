# Repository Guidelines

## Project Structure & Module Organization
- `src/pages/`: Route files (`.astro`, `.md`, `.mdx`). URL = filename (kebab-case). Example: `about-me.astro` → `/about-me`.
- `src/components/`: Reusable UI components. Prefer `PascalCase.astro`.
- `src/content/`: Markdown/MDX collections (e.g., `blog/`). Frontmatter: `title`, `description`, `pubDate`, `updatedDate`, `draft`.
- `src/layouts/`: Page/post layouts.
- `public/`: Static assets served as-is.
- `dist/`: Build output (do not edit).

## Build, Test, and Development Commands
- `pnpm install`: Install dependencies. Requires Node.js 18+ and pnpm 8+.
- `pnpm dev`: Start dev server at `http://localhost:4321`.
- `pnpm build`: Production build into `dist/`.
- `pnpm preview`: Serve the built site locally.
- `pnpm astro check`: Type and diagnostics check for `.astro`, TS, and content.

## Coding Style & Naming Conventions
- Indentation: 2 spaces; UTF-8; LF line endings.
- Components: `PascalCase.astro`; colocate simple helpers near usage.
- Routes/pages: kebab-case filenames (e.g., `about-me.astro`).
- Content slugs: kebab-case; keep frontmatter minimal (see above).
- CSS: Prefer scoped styles in `.astro`; use utility classes sparingly.
- Imports: Prefer absolute from `src/` when clearer; otherwise relative.

## Testing Guidelines
- Primary check: run `pnpm astro check` before pushing.
- No test framework configured. If adding tests, propose `vitest` + `@astrojs/check` in a PR first.
- For content collections, validate frontmatter and run a local build to catch schema errors.

## Commit & Pull Request Guidelines
- Commits: Imperative, present-tense subject (72 chars max). Prefer Conventional Commits.
- Example: `feat(blog): add pagination to index`.
- PRs: Clear description, linked issue (if any), screenshots/GIFs for UI changes, and a checklist of affected pages. Keep PRs focused and small.

## Security & Configuration Tips
- Do not commit secrets. Only place publicly safe files in `public/`.
- Optimize images; prefer `public/` or content co-location with proper import paths.

## Agent-Specific Instructions
- Keep changes minimal and scoped to the task; match existing patterns and structure.
- Avoid introducing new tooling without discussion. Update docs when behavior or structure changes.

