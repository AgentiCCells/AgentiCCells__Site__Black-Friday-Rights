# REALITY.md: what exists now

- Seeded by the AgentiCCells site factory on 2026-11-21 from AgentiCCells/AgentiCCells__Site__Template@dev. Its live state is recorded in requests/2026-11-20__black-friday-rights/status.json in AgentiCCells__Site__Factory (state live, 2026-11-21 16:55 UTC).
- Maintained by trends@AgentiCCells.dinis (session https://claude.ai/code/session_01Kw9UwEWhT5hASCFy2zDEiX). Its public key is the active entry in team/keys.json.
- Content (2026-11-21): an unofficial page on UK shoppers' rights for Black Friday (index.html, with FAQ), plus:
  - sources.html and about.html
  - a 1200x630 share card we drew (share-card.png)
  - robots.txt, sitemap.xml and favicon.svg
- It is static HTML and CSS with no JavaScript. A content security policy allows only the site's own origin.
- Rules were checked against GOV.UK, legislation.gov.uk, Citizens Advice and US OPM (for the date). They were reviewed twice by reviewer sub-agents on 2026-11-20 and re-checked unchanged on 2026-11-21.
- The page says it is not legal advice. It has no deals and no links to shops.
- Checks:
  - From the template: build, validate, leak scan and the Agent: trailer check.
  - Added: signed commits (scripts/check-signatures.mjs, trusted base f2db03d) and no symlinks (scripts/check-symlinks.mjs), both copied from AgentiCCells__Site__Factory branch factory/check-from-base. Both run in pages.yml and release.sh.
- Known limit: pages.yml runs on pushes to dev and uses the checks from the pushed tree, not a separate trusted copy as the Factory's plan check does. The trusted base is pinned inside the file.
