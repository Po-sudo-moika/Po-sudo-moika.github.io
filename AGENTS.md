# Po-sudo-moika.github.io

A personal GitHub Pages user site, live at https://po-sudo-moika.github.io. It is a static site built by Astro.

## Build and deploy

- `.github/workflows/deploy.yml` builds the site with `withastro/action` and deploys it with `actions/deploy-pages`.
- It runs on every push to `main`, and can be run by hand from the Actions tab. Pull requests build the site but do not deploy it.
- The workflow's `node-version` is the one Node version pin for the project.

## Preview locally

Run `npm install`, then `npm run dev`, and open the URL it prints. `npm run build` writes the built site to `dist/`.

## Where content lives

- `src/pages/index.astro` is the home page.
- Any other page goes in `src/pages/` as an `.astro` or `.md` file. Static files go in `public/`.
- Astro publishes only pages in `src/pages/`, files in `public/`, and what those pages import. Agent files (`AGENTS.md`, `CLAUDE.md`, `GLOSSARY.md`, `docs/`) live outside them, so they are not published. Keep new non-site files out of `src/pages/` and `public/`.

## Agent skills

### Issue tracker

Issues live in this repo's GitHub Issues (`gh` CLI). See `docs/agents/issue-tracker.md`.

### Triage labels

The five default labels: `needs-triage`, `needs-info`, `ready-for-agent`, `ready-for-human`, `wontfix`. See `docs/agents/triage-labels.md`.

### Domain docs

Single-context: one `GLOSSARY.md` and `docs/adr/` at the repo root. See `docs/agents/domain.md`.
