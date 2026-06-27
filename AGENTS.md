# Global Agent Instructions

## Office document handling — officecli first (overrides skill examples)

For ANY read or write of a `.docx`, `.xlsx`, or `.pptx` file, use the `officecli` CLI — **even when an invoked skill's examples show python (openpyxl / python-docx / python-pptx) or LibreOffice**. This rule outranks skill body content per instruction priority (user instructions > skills > system).

- Applies to all finance skills (financial-analysis, earnings-reviewer, model-builder, investment-banking, pitch-agent, etc.) and document-skills (docx/xlsx/pptx).
- The actual document read/write goes through officecli. Run `officecli load_skill <name>` (word/excel/pptx/financial-model/pitch-deck/...) for the matching subskill first.
- **Exception:** defer to the skill's python when it does non-document work the CLI can't express — e.g. pandas/numpy math, data cleaning, statistical modeling. Only the Office file I/O is redirected to officecli, not the computation.
- If officecli genuinely cannot express an operation, fall back to the skill's method and say so.

## PDF handling — lit first

For reading or extracting text/tables/values from PDFs, use the `lit` CLI (liteparse) via the `effective-liteparse` skill. Fall back to pypdf/pdfplumber/pdftotext only for structural ops (merge, split, rotate, create, watermark, forms, OCR scanned docs).

