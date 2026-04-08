# CV Repo

Single-file academic CV (`cv.tex`), compiled with **XeLaTeX** (`xelatex cv.tex`).

## Conventions
- **Fonts:** Body text uses `lmodern`. Section headings and name use `Gill Sans` (via `fontspec`). Icons via `fontawesome5`.
- **Author name:** Always use `\myname` macro (renders as bold-italic).
- **Co-first authorship:** Mark with `*` after author names and add `(*equal contribution)` at end of author list.
- **Publication order:** Chronological, oldest to newest. Number with `[N]`.
- **Publication format:** `[N] Title \\ Authors \\ arxiv link (Venue)`.
- **Paper cross-references:** Research/Work Experience items reference papers as `[\textbf{paper N}]` matching publication numbers.
- **Last updated date:** Auto-generated via `\today`.
- **Footer:** Update "of N" if page count changes.

## Common Update Tasks

### Adding a new publication
1. Add entry in Publications section in chronological order, increment all subsequent `[N]` numbers.
2. Update all `[\textbf{paper N}]` references in Research Experience and Work Experience sections to match new numbering.
3. Add a bullet point in the appropriate Research/Work Experience section describing the contribution.

### Updating a preprint to accepted
Change `(\textbf{Preprint})` to `(\textbf{Venue Year})`, e.g., `(\textbf{ICML 2026})`.

### Adding a new research experience
Add a `\medskip\noindent` block with lab name, university, date range, supervisor, and itemized contributions.

### Adding new reviewer service
Append to the `\textbf{Reviewer:}` line in Academic Service, e.g., `ICML 2026, NeurIPS 2026`.

## Workflow
```bash
xelatex cv.tex
git add cv.tex cv.pdf
git commit -m "description"
git tag vX.Y
git push --tags
```
