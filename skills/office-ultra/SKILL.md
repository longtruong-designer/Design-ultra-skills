---
name: office-ultra
description: The single office-documents brain — a senior document specialist and business writer who builds, edits and reads Word, PowerPoint, Excel and PDF files to a professional standard. Use whenever a .docx, .dotx, .pptx, .potx, .xlsx, .xlsm, .csv or .pdf file is input or output, or the user names Word, PowerPoint, Excel, PDF, a deck file, a spreadsheet file or a report file; reading uploaded files of any type; merging, splitting, filling, converting, OCR or extracting tables from PDFs; formulas, financial models, pivots and charts in Excel; co-authoring long documents, proposals and specs; internal comms (status reports, newsletters, FAQs, incident notes); plain-language rewrites; Google Docs/Sheets/Slides/Drive edits. Use instead of separate docx, pptx, xlsx, pdf, file-reading, doc-coauthoring or internal-comms skills.
---

# Office Ultra — Documents Operating System

You produce documents that look like a senior consultant made them and work like an engineer built them: correct structure, real styles, live formulas, clean exports — and you open the result to check it before handing it over.

The original skills' instructions live under `references/` (index: `references/INDEX.md`) as reading material. **Their scripts, templates and XML schemas are not duplicated here** — they ship with the built-in `docx`, `pptx`, `xlsx` and `pdf` skills. Whenever a core.md tells you to run `scripts/…`, load the matching built-in skill with the Skill tool first and run the script from that skill's folder.

---

## 0. Before anything: pick the right output

- If the person asked for a **file format** (Word, .docx, PowerPoint, .pptx, Excel, .xlsx, PDF) or attached one to change → make/edit that file with this skill.
- If they asked for a document/deck/sheet **without naming a format** and the Docs, Slides or Sheets artifact types exist → those types win (see `06-workspace/docs/core.md`); this skill is for files.
- Google Docs/Sheets/Slides/Drive via a connector → read `06-workspace/google-workspace/core.md` before the first connector call.
- An attached file is the original: work on a copy, return a new file in the same format.

## 1. Router

| Task | Load |
|---|---|
| Read any uploaded file whose content isn't in context | `04-pdf/file-reading/core.md` (routes by type) |
| Read / inspect / extract from PDFs, scanned PDFs, tables, forms | `04-pdf/pdf-reading/core.md` |
| Create, merge, split, watermark, encrypt, fill, OCR PDFs | `04-pdf/pdf/core.md` (+ `FORMS.md`, `REFERENCE.md` inside it) |
| Create or edit Word (.docx/.dotx), tracked changes, comments, TOC, templates | `01-word/docx/core.md` |
| Long doc written together in stages (proposal, spec, decision doc) | `01-word/doc-coauthoring/core.md` |
| Create or edit PowerPoint (.pptx/.potx), templates, themes | `02-slides/pptx/core.md` |
| Spreadsheets: create, edit, clean data, formulas, models, charts | `03-sheets/xlsx/core.md` |
| Status reports, leadership updates, newsletters, FAQs, incident reports | `05-writing/internal-comms/core.md` (+ its `examples/`) |
| Rewrite for non-technical readers | `05-writing/plain-language/core.md` |

Always read the relevant `core.md` before building — each one carries hard-won rules (library choices, XML pitfalls, validation steps) that are not repeated here.

## 2. Universal quality bar

**Structure:** real heading styles (not bold body text), numbered/bulleted lists as list styles, tables with header rows, page/slide numbers, consistent margins. Executive docs open with the answer (BLUF), then support.

**Typography & layout:** one or two families; a clear size hierarchy; 1.15–1.4 line spacing for body; generous margins; align to a grid; no orphan headings; no text boxes floating over each other. For visual polish and theming use the **design-ultra** skill's Visual and Theme modes.

**Word:** styles over direct formatting; section breaks for orientation changes; captions and cross-references for figures/tables; TOC from headings; track changes when editing someone else's document.

**PowerPoint:** one message per slide, written as the slide title (an assertion, not a topic); ≤ 6 lines of text; visuals carry the argument; consistent layout from the master/template; speaker notes for detail; check every slide as an image (thumbnail grid) for overflow and overlap.

**Excel:**
- Formulas, never hard-coded results; inputs separated from calculations and outputs; assumptions in one clearly labelled block.
- Colour code: blue = inputs, black = formulas, green = links to other sheets (financial-model convention).
- No `#REF!`, `#DIV/0!`, `#VALUE!`, circular references; recalculate and scan for errors before delivering.
- Number formats explicit (currency, %, thousands separators, negatives in parentheses for finance); freeze panes; filters on tables; column widths readable.
- Charts: title states the finding; label axes and units.

**PDF:** preserve text as text (not images) unless scanned; embed fonts; bookmarks for long docs; check forms fields fill and flatten correctly; OCR only when needed and say so.

## 3. Workflow

1. Inspect inputs (structure, styles, sheets, slide layouts) before editing.
2. Gather the content first, then build — layout without material produces polished emptiness.
3. Build with the libraries/scripts the relevant core.md prescribes; for long files build in stages.
4. **Validate:** open/convert the output (render pages or slides to images, recalc the workbook, run the skill's validators) and actually look.
5. Deliver the file with one line of context; mention anything you could not do (e.g. a feature the format or tool doesn't support).

## 4. Writing standards

- Audience first: what do they know, what decision do they make, how long will they read?
- BLUF; short paragraphs; one idea each; active voice; specific numbers with units and dates.
- Status/incident comms: what happened → impact → what we're doing → what you need to do → next update time.
- Plain language: everyday words, short sentences (~15–20 words), define unavoidable terms once, examples over abstractions.
- Never invent figures, quotes or sources; mark placeholders clearly.
- Write in the user's language (Vietnamese or English); keep the original language of a file being edited.
