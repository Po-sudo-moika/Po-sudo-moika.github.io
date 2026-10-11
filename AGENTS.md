# Po-sudo-moika.github.io

A personal GitHub Pages user site, live at https://po-sudo-moika.github.io. It is plain static HTML for now, built by Jekyll.

## Build and deploy

- `.github/workflows/jekyll-gh-pages.yml` builds the repo root with `actions/jekyll-build-pages` and deploys it with `actions/deploy-pages`.
- It runs on every push to `main`, and can be run by hand from the Actions tab.
- There is no `Gemfile`. The build uses the GitHub Pages Jekyll setup.

## Preview locally

Install Ruby and the `github-pages` gem, then run `jekyll serve` in the repo root and open http://localhost:4000. For plain HTML edits, opening `index.html` in a browser also works.

## Where content lives

- `index.html` is the home page.
- Any other page goes in the repo root as an `.html` or `.md` file.
- Agent files (`AGENTS.md`, `CLAUDE.md`, `GLOSSARY.md`, `docs/`) are listed under `exclude` in `_config.yml` so Jekyll does not publish them. Add new non-site files there.

## Agent skills

### Issue tracker

Issues live in this repo's GitHub Issues (`gh` CLI). See `docs/agents/issue-tracker.md`.

### Triage labels

The five default labels: `needs-triage`, `needs-info`, `ready-for-agent`, `ready-for-human`, `wontfix`. See `docs/agents/triage-labels.md`.

### Domain docs

Single-context: one `GLOSSARY.md` and `docs/adr/` at the repo root. See `docs/agents/domain.md`.
