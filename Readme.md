# Knowledge base

Onboarding, employee handbook, HR guides, IT help, company policies, and department runbooks. This documentation site is built with [Mintlify](https://mintlify.com).

## Project structure

- `docs.json` — site configuration (theme, navigation, colors)
- `index.mdx` — landing page
- `onboarding/` — first day, first week, and tooling guides
- `hr-people/` — benefits, compensation, performance, and time off
- `it-security/` — access requests, device policy, and security training
- `policies/` — code of conduct, expenses, remote work, and travel
- `engineering/` — architecture, deployment, dev setup, and incident response
- `logo/`, `images/`, `favicon.ico`, `style.css` — branding and styling assets
- `AGENTS.md` — instructions for AI agents working in this repo

Pages are MDX files with YAML frontmatter. Edit content in place and update navigation in `docs.json`.

## Local development

Prerequisites: Node.js 18+ and the [Mintlify CLI](https://www.npmjs.com/package/mint).

Install the CLI once:

```bash
npm i -g mint
```

From the repo root:

```bash
mint dev
```

The site is served at `http://localhost:3000` with hot reload.

## Validate before pushing

```bash
mint validate       # checks docs.json and frontmatter
mint broken-links   # checks internal links
```

Fix any errors before opening a pull request.

## Contributing

1. Create a branch from `main`.
2. Make your changes — keep sentences concise, use active voice and second person, and use sentence case for headings.
3. Run `mint validate` and `mint broken-links`.
4. Open a pull request.

See `AGENTS.md` for the full style guide and conventions.

## Deployment

Merges to `main` trigger an automatic deploy to the production docs site.
