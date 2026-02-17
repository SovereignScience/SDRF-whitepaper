# SDRF Whitepaper

The Sovereign Data Research Fabric (SDRF) is a privacy‑first architecture for human‑subject research. It replaces copy‑and‑store data flows with compute‑to‑data so participants keep encrypted vaults under their control while researchers run approved analyses inside protected environments, releasing only privacy‑preserving outputs. SDRF combines cryptographic consent, verifiable credentials, threshold keying, confidential compute, and differential privacy into a coherent research stack designed for longitudinal, multimodal studies in sensitive domains.

Current release: Version 1.2 (February 17, 2026).

Read the PDF: [SDRF_whitepaper.pdf](SDRF_whitepaper.pdf)

## Abstract

SDRF is a privacy‑first architecture for human‑subject research that makes consent enforceable by code and keeps raw data under participant control. It enables researchers to analyze sensitive, multimodal signals without centralizing them by moving computation to participant‑controlled vaults and releasing only privacy‑protected results. The system is modular and decentralized, supports multi‑site collaboration, and is designed to scale rigorous science without creating centralized honeypots of the most intimate data humans produce.

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
