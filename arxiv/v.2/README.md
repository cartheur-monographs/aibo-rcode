# v.2 Paper Workspace

This folder is for material that is intended to be promotable into the next arXiv draft.

It now serves as the replacement candidate for `../../v.1/`.

Rules:

- keep text here conservative and citation-ready,
- only move claims here after they have been checked against sources or hardware evidence,
- avoid mixing speculative ideas directly into draft prose,
- if a paragraph depends on interpretation, link it back to a note in `../notes/`.

Suggested contents:

- `main.tex` or section-level LaTeX files for the next draft,
- figure captions that are ready for paper use,
- paper-safe summaries derived from the notes,
- claim tracking in `claim-ledger.md`.

Current bundle:

- `main.tex`: primary LaTeX source
- `main.pdf`: compiled draft
- `references.bib`: BibTeX database
- `generate_behavior_diagrams.py`: Graphviz generator for the figure ladder
- figure assets for `EmbodiedBehaviors`, `CTracking`, `BootSafePose`, `Move`,
  `ContactResponse`, `Maze`, and `Football`

Local build:

```bash
cd arxiv/v.2/paper
python3 generate_behavior_diagrams.py
pdflatex -interaction=nonstopmode -halt-on-error main.tex
bibtex main
pdflatex -interaction=nonstopmode -halt-on-error main.tex
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```

Current working title:

- `From ERS-111 Behavior Diagrams to Distributed Embodiment: SOFTSIM and GA144 as an Executable Framework`
