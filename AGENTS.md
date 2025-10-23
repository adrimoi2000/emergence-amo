# Repository Guidelines

Use this reference to onboard quickly while we finish scaffolding the landing page stack; treat every rule as the baseline unless the tech lead signs off on a documented exception.

## Project Structure & Module Organization
The site runs on a Vite-powered React + TypeScript setup. Keep production code under `src/`, grouping reusable UI in `src/components/`, page-level compositions in `src/sections/`, and shared utilities in `src/lib/`. Static assets (favicons, illustrations, social images) belong in `public/`. Long-form copy or data lives in `content/` so non-developers can edit without touching TSX. Storybook stories stay alongside components as `ComponentName.stories.tsx`. End-to-end helpers and fixtures go in `tests/e2e/`.

## Build, Test, and Development Commands
Install dependencies once with `npm install`. Run `npm run dev` for the hot-reloading dev server. Produce production bundles via `npm run build`. Lint with `npm run lint` before every PR; it runs ESLint + Prettier checks. Unit tests execute with `npm run test -- --watch=false` for deterministic CI runs, and `npm run preview` serves the production build locally to verify final assets.

## Coding Style & Naming Conventions
Use 2-space indentation, TypeScript strict mode, and the ESLint recommended+React preset. Prettier handles formatting; avoid manual alignment or local overrides. Name files and folders in kebab-case, React components in PascalCase, hooks as `useSomething`, and CSS modules as `ComponentName.module.scss`. Prefix custom data attributes with `data-amo-` to keep selectors unique, and export a single default per component file.

## Testing Guidelines
Vitest + Testing Library cover component behaviour; co-locate specs as `ComponentName.test.tsx`. Target ≥80% branch coverage and call out justified gaps in the PR description. Flows that span multiple steps need a Playwright spec in `tests/e2e/`, named after the user story (`hero-carbon.spec.ts`). Mock network boundaries with MSW to keep runs fast and deterministic.

## Commit & Pull Request Guidelines
Use Conventional Commits (`feat: add carbon footprint banner`) and keep changes atomic. Rebase on `main` before pushing to avoid merge commits. PRs require: a summary describing intent and trade-offs, linked issue or Linear ticket, screenshots or recordings for visual diffs, and a checklist of manual QA (desktop, mobile, accessibility). Secure at least one reviewer covering both design and engineering, and only merge on green CI.

## Security & Configuration Tips
Never commit `.env` files; provide sample keys in `env.example`. Rotate API tokens after each production incident. Run `npm audit` monthly and escalate high-severity CVEs to the maintainer within 24 hours.
