# SDRF Whitepaper

This repository contains the Sovereign Data Research Fabric (SDRF) whitepaper.

## Files

- `SDRF_whitepaper.md`: source Markdown
- `SDRF_whitepaper.pdf`: rendered PDF
- `pandoc_header.tex`: LaTeX header used for PDF styling

## Regenerate the PDF

Requirements:
- `pandoc`
- `xelatex` (TeX Live)

Command:

```bash
pandoc SDRF_whitepaper.md -o SDRF_whitepaper.pdf \
  --from markdown+pipe_tables+footnotes+autolink_bare_uris \
  --pdf-engine=xelatex \
  --include-in-header pandoc_header.tex \
  --metadata linkcolor=black --metadata urlcolor=blue \
  --metadata citecolor=black --metadata filecolor=blue \
  --metadata linkreferences=true
```
