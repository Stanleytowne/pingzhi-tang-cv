# Pingzhi Tang's CV

## Overview
This repo contains a single-file academic CV (`cv.tex`) compiled with **XeLaTeX**.

## Author
- **Name:** Pingzhi Tang (唐平之)
- **Affiliation:** Peking University, B.S. in AI (Tong Class), Sept 2023 – present
- **Email:** stanleytang@stu.pku.edu.cn
- **GitHub:** [Stanleytowne](https://github.com/Stanleytowne)
- **Google Scholar:** [UYRV6y0AAAAJ](https://scholar.google.cz/citations?user=UYRV6y0AAAAJ)
- **Homepage:** [pingzhitang.cv](https://pingzhitang.cv)

## Research Labs
- **M μ Lab** (Prof. Muhan Zhang) — July 2024 – present. Main lab, focus on efficient LLM methods.
- **PKU-SEC-Lab** (Prof. Meng Li) — Sept 2025 – Feb 2026. Focus on Diffusion LLM acceleration.
- **Tencent** (industry intern) — June 2025 – Sept 2025. MLA tensor parallelism.

## CV Structure (section order in cv.tex)
1. Education
2. Research Interests
3. Publications (chronological, oldest first)
4. Research Experience
5. Work Experience
6. Skills
7. Academic Service
8. Achievements

## Conventions
- **Compiler:** XeLaTeX (`xelatex cv.tex`)
- **Fonts:** Body text uses `lmodern`. Section headings and name use `Gill Sans` (via `fontspec`). Icons via `fontawesome5`.
- **Colors:** `headerblue` RGB(31,73,105), `linkblue` RGB(38,103,138).
- **Author name:** Always use `\myname` macro (renders as bold-italic "Pingzhi Tang").
- **Co-first authorship:** Mark with `*` after author names and add `(*equal contribution)` at end of author list.
- **Publication order:** Chronological, oldest to newest. Number with `[N]`.
- **Publication format:** Each entry has: `[N] Title \\ Authors \\ arxiv link (Venue)`.
- **Paper cross-references:** Research/Work Experience items reference papers as `[\textbf{paper N}]` matching publication numbers.
- **Last updated date:** Auto-generated via `\today` — no manual updates needed.
- **Footer:** Shows "Pingzhi Tang -- Page X of 2" (update "of 2" if page count changes).

## Workflow
After making changes:
```bash
xelatex cv.tex
git add cv.tex cv.pdf
git commit -m "description"
git tag vX.Y
git push --tags
```

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
