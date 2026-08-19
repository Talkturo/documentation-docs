# Talkturo documentation

Source for the Talkturo product docs: bilingual MDX pages plus the navigation config that drives the docs site.

## What’s in this repo

| Path | Purpose |
| --- | --- |
| [`documentation.json`](documentation.json) | Site config: name, colors, and navigation for **English** and **German**. Page titles, tabs, groups, and paths live here. |
| [`en/`](en/) | English docs (`*.mdx`) and [`en/api-reference/openapi.yaml`](en/api-reference/openapi.yaml). |
| [`de/`](de/) | German docs with the **same folder and file names** as `en/`, plus a translated OpenAPI spec. |

Internal links in MDX must include the locale prefix (`/en/...` or `/de/...`) so they don’t resolve to an empty path.

## Content map

Both locales follow the same layout:

- **Product docs** — getting started, assistants, campaigns, telephony, CRM, TurboFlow, Close AI Desktop, billing, integrations
- **API reference** — REST docs under `api-reference/` plus OpenAPI
- **Help Center** — FAQs, troubleshooting, guides
- **Changelog** — `changelog.mdx`

## Conventions

- Keep `en/` and `de/` in sync: same relative paths, same MDX structure.
- Translate body copy and navigation labels in `documentation.json` for German; keep file names and `operationId`s unchanged.
- API paths, code samples, product names, and schema keys stay as in the product.
- Billing copy should mention **Stripe** only (no legacy payment providers).
