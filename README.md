# Reasoning Lab · Peds (working name)

WCM-internal pediatrics learning platform prototype.

## Layout

- docs/ is the only folder that is published. Student-facing pages only: index.html, the Kayla Novak and Megan Morris cases, the two resource pages, normal-values.json, and the Kayla handout. Files sit side by side because the pages link to each other by file name.
- cases/ holds case sources: agent prompts, knowledge banks, rubrics, authoring sheets, test results. Not published.
- grading/ holds the checklist and the script that pulls grades. Faculty only. Not published.

## Publishing

Settings, Pages, Deploy from a branch, branch main, folder /docs. The site address is then https://mnhillard-wq.github.io/MedEd/.

## Rules

- Build only from work created after 30 April 2026. Check each case against the Post-Disclosure Work Ledger before adding it.
- Nothing from the grading checklist or rubrics goes in docs/.
- Pages serves a public address even when the repository is private, unless the account is on GitHub Enterprise Cloud.
