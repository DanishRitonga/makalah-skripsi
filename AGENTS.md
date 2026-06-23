# AGENTS.md

IEEE conference paper (LaTeX) using `IEEEtran.cls`. "RayCastED: Lightweight and Boundary-Aware Nuclei Detection Model for Histopathology Images".

Shorter version of the full thesis (`/home/danishrtg/projects/RayCastED-undergraduate-thesis`). Covers only core content:

- **Introduction**: problem, motivation, contributions
- **Methodology**: model architecture and training design (no data preprocessing)
- **Results**: experimental findings
- **Conclusion**

Data modelling is in scope; data preprocessing is not.

## Build

```bash
pdflatex main.tex && bibtex main && pdflatex main.tex && pdflatex main.tex
latexmk -pdf main.tex   # shorter alternative
```

Uses **pdflatex** (not xelatex/lualatex). `IEEEtran.cls` and `cite` package are standard.

## Key files

- `main.tex`: single-file paper (all content inline, no `\include`)
- `IEEEtran.cls`: IEEEtran v1.8b bundled locally (do not modify)
- `references.bib`: BibTeX entries; bib style: `IEEEtran`
- `fig1.png`: placeholder figure

## Conventions

- `\documentclass[conference]{IEEEtran}` with two-column layout
- `\IEEEoverridecommandlockouts` is enabled (needed for funding footnote)
- Author fields contain placeholder names. Do not fill in real personal data
- Content is still largely the IEEE template boilerplate; real paper content replaces sections in place
- The thesis `contents/chapter-1/sketch-1.md` outlines the intended argument flow for the introduction. Follow it when editing the Introduction section

## Writing style (reviewer requirements)

Tense by section:
- **Introduction/Background**: simple present (established facts, general context)
- **Purpose/Objective**: simple present or present perfect
- **Methodology**: simple past (completed actions)
- **Results**: simple past (specific findings)
- **Conclusion/Implications**: simple present (interpretation, broader meaning)

Additional rules:
- Avoid "this" pointing to an experiment, result, or tool. Use "this" only to refer to the paper, study, or topic
- Avoid "will" (implies future tense)
- Avoid "we" (not universally acceptable in IEEE conference style)

## Companion repos

- Full thesis: `/home/danishrtg/projects/RayCastED-undergraduate-thesis` (report class, multi-file)
- Model implementation: `/home/danishrtg/projects/RayCastED/`
