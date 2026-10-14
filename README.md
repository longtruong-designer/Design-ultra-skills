# Ultra Skills

Seven consolidated Claude skills. Each one replaces a cluster of single-purpose skills with one "brain" (`SKILL.md`: expert operating principles + a mode router) and a `references/` library holding the full source skills it routes to.

| Skill | Replaces | Package |
|---|---|---|
| **design-ultra** | design, design-skills, frontend-design, ui-ux-pro-max (full database + scripts), taste-skill, Impeccable playbooks, Emil Kowalski design engineering, ui-skills, awesome-design-md (84 DESIGN.md files), Vercel Web Interface Guidelines, theme-factory, canvas-design and related | `dist/design-ultra.skill` |
| **engineering-ultra** | engineering, 10x-Team, zizi (code), shieldcode, serverless-audit, mcp-builder, modern-web-guidance and related | `dist/engineering-ultra.skill` |
| **product-ultra** | product-management, planning, A/B testing, product-tracking, status/handoff | `dist/product-ultra.skill` |
| **marketing-ultra** | marketing, searchfit-seo, competitive intel, brand listening, postiz | `dist/marketing-ultra.skill` |
| **sales-ultra** | sales, zime-skills, prospecting | `dist/sales-ultra.skill` |
| **office-ultra** | docx, pptx, xlsx, pdf, file reading, doc co-authoring, internal comms (scripts are used from the built-in skills) | `dist/office-ultra.skill` |
| **research-ultra** | deep-research, research methods, Bright Data search/scrape/feeds, analytics | `dist/research-ultra.skill` |

## Layout

```
dist/      ready-to-upload .skill packages (zip)
skills/    the same skills unpacked, for reviewing changes
```

## Install

Upload each file in `dist/` to Claude under Settings → Skills. After installing, turn off the plugins and single skills each Ultra skill replaces so they don't compete to trigger.

## Rebuild a package after editing `skills/<name>/`

```bash
python -m scripts.package_skill skills/<name> dist   # from Anthropic's skill-creator
```

Keep packages free of hidden files, caches (`__pycache__`, `*.pyc`), archives and binaries — those break uploads.

## Licensing

See [NOTICE.md](NOTICE.md). The bundled third-party material keeps its own license; the root `LICENSE` does not apply to it.
