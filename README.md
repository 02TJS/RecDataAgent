# RecDataAgent

Anonymous ICLR manuscript source for **RecDataAgent: User-Conditioned Data Augmentation for LLM-based Recommendation**.

## Contents

- `main.tex`: manuscript entry point
- `sections/`: manuscript sections and tables
- `figures/`: figures referenced by the manuscript
- `references.bib`: bibliography
- `template/`: required ICLR style and bibliography files

## Build

Install a TeX distribution with `pdflatex` and `bibtex`, then run:

```text
pdflatex -interaction=nonstopmode -halt-on-error -output-directory=build main.tex
bibtex build/main
pdflatex -interaction=nonstopmode -halt-on-error -output-directory=build main.tex
pdflatex -interaction=nonstopmode -halt-on-error -output-directory=build main.tex
```

On Windows PowerShell, set the local template search paths before compiling:

```powershell
$env:TEXINPUTS = "template;$env:TEXINPUTS"
$env:BSTINPUTS = "template;$env:BSTINPUTS"
$env:BIBINPUTS = ".;$env:BIBINPUTS"
```

The manuscript is anonymized for double-blind review. No datasets, model
weights, checkpoints, execution logs, or machine-specific paths are included.
