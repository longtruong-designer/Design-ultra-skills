# Notice — third-party material

The root `LICENSE` (CC0 1.0) covers only the original files written for this repository: each skill's top-level `SKILL.md`, the `references/INDEX*.md` files, `README.md` and this notice.

Everything under `skills/*/references/` (and the same files inside `dist/*.skill`) was consolidated from other skills and **keeps its original license**. It is not CC0.

## Open-source sources (bundled with their license files)

| Location | Source | License |
|---|---|---|
| `skills/design-ultra/references/11-taste-and-web/taste-skill` | github.com/Leonxlnx/taste-skill | MIT |
| `skills/design-ultra/references/11-taste-and-web/impeccable` (reference playbooks only) | github.com/pbakaus/impeccable | Apache-2.0 |
| `skills/design-ultra/references/11-taste-and-web/design-taste` | github.com/h3nryprod01/design-taste | MIT |
| `skills/design-ultra/references/11-taste-and-web/ui-skills` | github.com/ibelick/ui-skills | MIT |
| `skills/design-ultra/references/11-taste-and-web/emil-design-engineering` | github.com/emilkowalski/skills | MIT |
| `skills/design-ultra/references/11-taste-and-web/vercel-web-interface-guidelines` | github.com/vercel-labs/web-interface-guidelines | MIT |
| `skills/design-ultra/references/04-visual/ui-ux-pro-max-full` | github.com/nextlevelbuilder/ui-ux-pro-max-skill | MIT |

## Anthropic and plugin skills

The remaining reference folders come from skills installed in the owner's Claude account: Anthropic's built-in skills (for example docx, pptx, xlsx, pdf, frontend-design, canvas-design, theme-factory, deep-research) and third-party plugins (for example design-skills, engineering, 10x-Team, zizi-skills, sales, zime-skills, searchfit-seo, Bright Data, product-tracking). Each source folder is named after the skill it came from, and most `core.md` files built from installed skills start with a `<!-- source skill: plugin:skill -->` comment.

Anthropic's built-in skills state "© Anthropic, PBC. All rights reserved" and are governed by Anthropic's terms of service. Plugin skills are governed by their publishers' terms.

**Keep this repository private.** Before making it public or sharing it, remove or replace the Anthropic and plugin material, or confirm each publisher's terms allow redistribution.
