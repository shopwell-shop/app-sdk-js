# AGENTS.md

## General

- Use conventional commit for commits and pull request title
- Project uses biome for formatting, linting: `npm run lint` fixing: `npm run lint:fix`
- Project is fully in TypeScript written and can be type checked with `npm run typecheck`

## Shopwell fork guardrails (mandatory)

This repository is the Shopwell fork of the upstream Shopware App SDK for
JavaScript. It is maintained and branded per `../sync-upstream/branding-map.md`
and the control plane in `../sync-upstream` (see its `AGENTS.md`).

- Shopwell-owned code is licensed under the Apache License 2.0; see `LICENSE`.
- Project-owned manifests must declare `Apache-2.0`.
- Registered project-owned `LICENSE` files (`LICENSE`, `src/LICENSE`) contain
  the standard Apache-2.0 text.
- Original upstream legal text (MIT, shopware AG) is preserved verbatim in the
  root `NOTICE`; do not brand, shorten, delete, or move it.
- Before commit, push, release, or sync completion, run:
  `../sync-upstream/bin/syncctl audit-license app-sdk-js` and
  `../sync-upstream/bin/syncctl audit-upstream-dependencies app-sdk-js`.
- Runtime code and workflows must not depend on `shopware/*`, `shopwarelabs/*`,
  `@shopware-ag/*`, or their GitHub repositories.
- The wire protocol names (`shopwell-app-signature`,
  `shopwell-shop-signature`, ...) intentionally match the Shopwell platform —
  both sides of the protocol are Shopwell-owned.
